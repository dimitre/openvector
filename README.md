# OpenVector File Format
author: Dimitre Lima  
url: https://dmtr.org/  
date: 2026 01m 08d  
version: 0.3  

## Intro
A new, open and universal vector format.

## Definitions
it should be human readable / editable  
Most open license possible (suggestion CC-0)

## Format
Based in an open and known file format.  
YAML suggested.

## Priority order
Start with rectangles and polylines  
Bezier representation can be identical to SVG notation  
It should also have a mode of storing everything as integer ratios, so infinite resolution is possible.   Optional fallback to float.

## General ideas.
Metadata section (creator, date, title, version, license, description, url, dimensions)
Objects can have an hierarchical structure, and common properties for all, like position and dimensions.  optionally scale and matrix transformations. optional name for any object including groups.
Z-order can be the sequence of the document itself or a parameter. it can also be both. sequence first, parameter second.  
Multiple canvas allowed with positioning for each, maybe allowing even overlapping. Freehand Style.  
A "drawer" object that works like a canvas but don't draw anything. useful for instancing a known object into multiple canvases with position and scale (all matrix transformation really).  
Instanced objects allowed. A general "drawer" object to store objects to be instanced in any canvas.

## Methodology
Developing only simple objects and properties first, like (ellipse, rectangle, fill and stroke) can help defining well the whole skeleton of any object. When everything is solid there more objects can be added spanning from a solid structure (text, gradients, etc).

## More
Implement Spiro curves format or Spline format.

## Potential Application
rust, openFrameworks, p5js, online vector editors, macos quicklook plugin, web backend

## LLM usage
Draft a file with a smile face with your take on this spec

Ideas are welcome.
