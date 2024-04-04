# Reference Documentation

## Globals Docstrings

::: molecule_lib.GLOBALS_DOCSTRINGS
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: false 
      docstring_section_style: list

## Math functions

::: molecule_lib.csc
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.sec
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.cot
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib._isfloatstr
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list


## ABC (Unitcell) Molecule Section

::: molecule_lib.ABCCoord
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
      members:
        - line

::: molecule_lib.LatticeMatrix
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true   
      docstring_section_style: list 
      members:
        - getabc
        - getanglesdeg
        - getanglesrad

::: molecule_lib.ABCMolecule
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true
      docstring_section_style: list
      members:
        - add_coords
        - append
        - convert
        - delete
        - freeze_atoms
        - format
        - get_centroid
        - info
        - manipulate
        - move
        - printt
        - rotate
        - save
        - sort
  
## ABC Private Functions

::: molecule_lib._islatticematrix
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib._is3byxfloatmatrix
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib._is6byxfloatselectivematrix
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

## ABC Functions

::: molecule_lib.isvasplist
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.create_from_vasp_file_data
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.read_vasp
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

## XYZ (No Unitcell) Molecule Section

::: molecule_lib.XYZCoord
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
      members:
        - line

::: molecule_lib.XYZMolecule
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true   
      docstring_section_style: list 
      members:
        - add_coords
        - append
        - convert
        - delete
        - format
        - get_centroid
        - info
        - manipulate
        - move
        - printt
        - rotate
        - save
        - sort

## XYZ Functions

::: molecule_lib.isturbomolelist
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.create_from_turbomole_file_data
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.read_turbomole
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
            
::: molecule_lib.isxyzlist
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.create_from_xyz_file_data
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.read_xyz
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
  
## More File Reading Formats

::: molecule_lib._is_xsf_coord_line
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib._determine_rest_of_xsf_file
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.isxsflist
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
            
::: molecule_lib.create_from_xsf_file_data
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.read_xsf
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.issiestalist
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
     
::: molecule_lib.create_from_siesta_file_data
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list

::: molecule_lib.read_siesta
    handler: python
    options:
      docstring_style: numpy
      show_root_heading: true
      heading_level: 3
      show_source: true
      summary: true    
      docstring_section_style: list
