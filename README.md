# GOPY
GOPY is an open source python code for building graphene and graphene oxide sheets, obtained from here: https://github.com/Iourarum/GOPY
There is also a paper available here: https://doi.org/10.1016/j.softx.2020.100586

This repository includes my modified version of GOPY: GOPY_V2.py
The purpose of this version is to build graphene oxide sheets that are periodic.

The function "def get_map_edge(atom_list):" on lines 350-364 have been edited, such that the edge detection of GOPY does not include carbons within 2 Angstroms of the periodic boundary conditions. This ensures no COOH groups are added to the edges of the flake, when the graphene sheet is intended to be periodic in the x and y directions. COOH groups will only be added to the internal voids, as defined by the new function on line 360: "def is_internal_void(atom):"

The remainder of GOPY functionality is the same as the original version.
