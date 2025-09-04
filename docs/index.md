---
hide:
  - navigation
  - toc
---
# Welcome to molecule_lib Documentation

This is a library dedicated to manipulating and creating molecular structures using python for theoretical chemistry.
Any feedback or bugs please email jerschro@ttu.edu or jeremynschroeder@gmail.com
Created by Jeremy Schroeder © 2024

For Reporting Bugs go to [https://github.com/jerschro/molecule_lib_documentation/issues](https://github.com/jerschro/molecule_lib_documentation/issues) and create a new issue.

Click here for the [API Reference](reference/index.md) page.


## Popular User Guides To See molecule_lib's Versatile Functionality

<div class="grid cards" markdown>

-   New to molecule_lib?

    ---

    If you are a new user to molecule_lib, check out this 5 minute read on what molecule_lib can do.

    [:octicons-arrow-right-24: Short Intro](user_guides/short_intro.md)

-   LAMMPS Functionality

    ---

    Check out examples of how molecule_lib can help automate input and output files for a popular Molecular Dynamics program, LAMMPS.

    [:octicons-arrow-right-24: LAMMPS](user_guides/lammps.md)

-   Complex Creation

    ---

    Check out how to create complex models easily using molecule_lib. Novel Functionality for molecule_lib!

    [:octicons-arrow-right-24: Complexes](user_guides/complexes.md)

-   Cluster Creation

    ---

    See how to create a electronic structure cluster model from a periodic slab model. Novel Functionality for molecule_lib!

    [:octicons-arrow-right-24: Clusters](user_guides/clusters.md)

</div>

## To install molecule_lib 

You can install the library directly from PyPI:

```bash
pip install molecule_lib

```

Requirements: Python 3.10 or later and Numpy. RDKit is optional but suggested.

RDKit is an optional dependency and can be installed separately via conda or pip:

```bash
conda install -c conda-forge rdkit
# or
pip install rdkit

```

<!-- ### Version/Module doc-string (developer info)
::: molecule_lib
    handler: python
    options:
      heading_level: 4 
      members:
      - __version__
      - __version_tuple__ -->
