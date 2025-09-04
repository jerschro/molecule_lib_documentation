---
hide:
  - navigation
---
[:fontawesome-solid-house:](../index.md) :fontawesome-solid-angle-right: **About**
# About molecule_lib

## History of development

This library was developed by Jeremy Schroeder at Texas Tech University Department of Mechanical Engineering in 2024.
It was created for the purposes of manipulating molecular structure files using scripts. 
There is a lack of ways to manipulate molecular files using scripts and Jeremy hopes that this library and documentation will help other molecular modelers not pull their hair out for manipulating molecular structures.

## Library Highlights

* There are two main objects to represent a molecular structure file, ABCMolecule and XYZMolecule.
* The LatticeMatrix object represents a unitcell/periodic boundary.
* There are two main objects that represent a 3d atomic position, ABCCoord and XYZCoord.
* You can read multiple different molecular file types and convert between each of them fast and efficient.
* Selecting a molecule to move or rotate in 3d space precisely.
* Ability to freeze specific atoms for particular DFT program inputs.
* Simply edit unitcell parameters. (Work in progress)
* Ability to reorder the atoms in a molecular structure file.
* Take popular DFT calculation output animations and convert to a filetype that popular molecular visualization programs can read.
* Ability to automate the creation of cluster models for electronic structure DFT calculations on surfaces.

## Mission

molecule_lib aims to lead the way in automating molecular file creation for molecular modelers. 
It also aims to be a resource for those learning object oriented programming and python type hinting as the implementation of oop is fairly simple. The library hopes to be a resource created by a molecular modeler, for molecular modelers to help make the work efficient and more productive.

## Citing molecule_lib

molecule_lib is open source licensed under the GNU GPL-3.0-or-later license. 

Please cite molecule_lib using the citation style below:

* Authors: Jeremy Schroeder, Adelia Aquino, Michelle Pantoya, Daniel Tunega
* Title: Introducing molecule_lib: a python library dedicated to automate computational chemistry model creation and manipulation.
* Journal: To Be Determined
* Date Published: To Be Determined