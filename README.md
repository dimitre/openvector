# OpenVector File Format

## Intro
The idea is making a new, open and universal vector format.

## Definitions
Most open license possible
it should be human readable / editable


## Format
Based in an open and known file format. I suggest YAML.

## Priority order
Start with rectangles and polylines
Bezier representation can be identical to SVG notation
It should also have a mode of storing everything as integer ratios, so infinite resolution is possible.

## General ideas.
Objects can have an hierarchical structure, and common properties for all, like position and dimensions. maybe scale.
Z-order can be the sequence of the document itself or a parameter. it can also be both. sequence first, parameter second.
Multiple canvas allowed with positioning for each, maybe allowing even overlapping. Freehand Style.
