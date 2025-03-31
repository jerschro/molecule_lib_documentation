[:fontawesome-solid-house:](../index.md) :fontawesome-solid-angle-right: [User Guides](index.md) :fontawesome-solid-angle-right: **Edit Vacuum**
# How to Edit the Vacuum of a Unitcell using molecule_lib

Using the method [ABCMolecule.edit_unitcell](../reference/ABCMolecule/edit_unitcell.md) we can add and subtract vacuum by creating a new [LatticeMatrix](../reference/LatticeMatrix/index.md) with the different. The below code is an example of how you create a slab with more or less vacuum. The slab is in the a and b plane and is normal to the c plane. The vacuum is in the c plane. The script automatically determines the slab thickness and adds and subtracts the vacuum dependent on the slab thickness. 

NOTE: You need to create a new [LatticeMatrix](../reference/LatticeMatrix/index.md) object in order for the method to work correctly.

``` python title="create_smaller_and_larger_vacuum.py"
from molecule_lib import *
slab = read_vasp("slab.vasp")

low_atom = slab.sort("z").get(1)
high_atom = slab.sort("z").get(-1)

diff_c = high_atom.c - low_atom.c
diff_z = diff_c * slab.unitcell.getabc()[2]

smaller_c = diff_z + 20 #create a vacuum of 20 angstroms
smaller_lm = LatticeMatrix(constant=slab.unitcell.constant,
                           vector_1=slab.unitcell.vector_1,
                           vector_2=slab.unitcell.vector_2,
                           vector_3=[0.0, 0.0, smaller_c])
smaller_vacuum = slab.edit_unitcell(new_unitcell=smaller_lm)
smaller_vacuum.to_vasp("smaller_vacuum.vasp")

larger_c = diff_z + 40 #create a vacuum of 40 angstroms
larger_lm = LatticeMatrix(constant=slab.unitcell.constant,
                           vector_1=slab.unitcell.vector_1,
                           vector_2=slab.unitcell.vector_2,
                           vector_3=[0.0, 0.0, larger_c])
larger_vacuum = slab.edit_unitcell(new_unitcell=larger_lm)
larger_vacuum.to_vasp("larger_vacuum.vasp")


```
