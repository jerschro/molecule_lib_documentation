# What is planned to be added to it in the future (aka TODO list)

1. Add support for lammps, and .cif
2. Add generate supercell method
3. Maybe change inplace ideology
4. Change logic for read functions so no extralines argument. It will be flexible on extra lines at the end of the file.
6. Add documentation for everything and maybe an examples page and an intro page
7. Maybe change how add_coord function works.


## Notes from word document
Shift alt o for formatting import statements
Ideas for structmake
#Pip install xtb
#Run xtb locally first
Then run crest on hpcc using submission script
•	Still two main molecule objects (abcmolecule and xyzmolecule) but there will be a specified initial file type
•	DONE(not using dataclasses anymore lol) Might need to not use dataclasses in order to stop the linking objects that occurs
For coord objects
•	Add a .get() method for coord data classes that returns (x,y,z)
For read_filetypes()
•	Raise ParserError when something goes wrong
•	Setting extralines: bool = False, strict on extra lines at EOF
•	Index = -1 , default
•	Different filetypes im looking at
o	.xyz 
o	.vasp/POSCAR
o	.xyz animation
o	.vasp animation/XDATCAR
o	.cif
o	.xsf
o	.fdf
o	Others: .json, .sdf not really sure if there is a common format
For Molecule objects
•	__get_item__(self) :If you index the molecule object [] it returns a new object with the atoms you selected. Based loosely on pandas indexing
o	Index types, first index is 1 (not python convention but makes sense in use case)
	Done
	Int – indexing is 1
	‘Al’ – all singular species type
	‘Al1’ – VESTA naming 
	‘1’ - int
	List of int [1,3,4,5,8,9,10,11]
	List of str
•	[‘Al’,’F’] – all species type
•	[‘1’,’2’,’3’] atom_number (covers molden numbering style without the species in it)
•	[‘Al1’,’O3’] vesta numbering style
	Not implemented yet
•	Range of int [1:20]
•	Add method similar to .format() but  Do .to_xyz(),.to_poscar(),.to_fdf()… , then in the save(filepath,filetype=init_filetype,optional: optional: selectivedynamicstag, ). Probably better to
o	Errors: if path directory doesn’t exist
o	Errors: if other information is not passed
•	.to_direct(lattice_matrix=)),.to_positional(lattice_matrix=)
o	Convert to positional coordinates. If cartesian molecule, you will need to pass lattice_matrix information either in dictionary form, {‘lattice_constant’:1.0,’lattice’:[[2,0,0],[0,2,0],[0,0,2]]} or {constant:1.0,vector_1:[2,0,0],vector_2:[0,2,0],vector_3:[0,0,2]}or in list/tuple form [1.0, [2,0,0],[0,2,0],[0,0,2]] or as the LatticeMatrix object as LatticeMatrix(constant=1.0,vector_1=[2,0,0],vector_2=[0,2,0],vector_3=[0,0,2]).
•	.to_cartestian()
o	Converts to cartesian coordinates.
•	Can have the convert() method which will use the other methods to_cartesian() and to_direct()
•	.move(x:float,y:float,z:float)
o	Returns object with moved atoms
•	.rotate(axis:int | literal[‘x’,’y’,’z’], angle: float, units:str = ’deg’, or ‘rad’)
o	Returns rotated object
•	 .delete(index, placeholder:bool=False)
o	When placeholder is active, it replaces the selected atoms with a placeholder coord CoordType(sp=’Zz’,x=…,y=…,z=….)
o	Returns molecule object with deleted atoms
•	.manipulate(index, function:str=’move’ | ‘rotate’,*args,**kwargs]
o	Would then pass *args,**kwargs to the .move()/.rotate() method.
o	Have to check if if default arguments are provided, if 
TODO
•	DONE Add endline argument to format() (to reuse it with print command)
•	DONE Create a print method that prints to terminal. Name it print()?
•	Figure out selective coords and dynamics
•	Add to_cartesian(), to_positional(), to_direct()
•	DONE Fix ABCmolecule printout, (need to add vasp specific attributes)
•	DONE Figure out a definite way of having positional/cartesian coordinates in abcmolecule
•	DONE Ensure every method and function has a doc string.
•	Add read_poscar function that is mask for read_vasp function
•	Maybe add abcanimation and xyzanimation so that there is a difference between them and it functions will be read_xdatcar() read_xyz_animation() read_vasp_animation(). We could add all other methods but really only need the index __setitem__() and convert().
•	Add delete placeholder argument, maybe add a replace option that will replace the place holder with a new atom?
•	Maybe add method add_centroid(inplace=False) that adds a centroid coord as a placeholder. 
•	Switch over lattice matrix to non dataclass
•	Create a determine molecule function, to determine the filetype of the molecule and it would return a reference to the class “return ABCMolecule”
•	Add inplace to delete()
