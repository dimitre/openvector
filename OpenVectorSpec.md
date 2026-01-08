# OpenVector File Format Specification
author: Dimitre Lima  
url: https://dmtr.org/  
date: 2026 01m 08d  
version: 0.5.5    

## Intro
A new, open and universal vector format.

## Definitions
it should be human readable / editable  
Most open license possible: CC-0

## Format
Based in an open and known file format: YAML.  
It should also have a mode of storing everything as integer ratios, so infinite resolution is possible.   Optional fallback to float.
Colors also can be stored as ratios, like 3/2
All coordinates and colours may be given as quoted rationals ‘p/q’ or plain scalars; parsers shall accept both

## General ideas.
Metadata section (author, generator (software), date, title, version, license, description, url, dimensions).  
Objects can have an hierarchical structure, and common properties for all, like position and dimensions.   optionally scale and matrix transformations. optional name for any object including groups.  
Z-order can be the sequence of the document itself or a parameter. it can also be both. sequence first, parameter second.  
Bezier representation can be identical to SVG notation.  
Multiple canvas allowed with positioning for each, maybe allowing even overlapping. Freehand Style.  
A "drawer" object that works like a canvas but don't draw anything. useful for instancing a known object into multiple canvases with position and scale (all matrix transformation really).  
Instanced objects allowed. A general "drawer" object to store objects to be instanced in any canvas.  

## Methodology
Developing only simple objects and properties first, like (ellipse, rectangle, fill and stroke) can help defining well the whole skeleton of any object. When everything is solid there more objects can be added spanning from a solid structure (text, gradients, etc).  

## Color
Starting with 8 bit RGB and hex notation #ff0033.   
CMYK, Grayscale or Spot named colors allowed.

## Versioning
Version format will only be useful during development.  
Once the specs are "locked in" one can only add more object / properties types.  
One list of basic capabilities is mandatory for writing / loading files, and additional capabilities can be marked as flags in metadata header so software can know if it can interpret everything or prompt user to load even without all implementation of the specific file.

## Extensibility
Custom types are allowed outside file specification using specially marked containers. So a CNC program can save/read specificities of application without breaking compatibility with the rest that can gracefully ignore. Custom types should be preserved when reading / saving in other software.

## Future
Implement Spiro curves format or Spline format. Niche format doesn't need to be implemented everywhere

## Potential Application
rust, openFrameworks, p5js, online vector editors, macos quicklook plugin, web backend, CNC fabrication, etc.  

## LLM usage
Draft a file with a smile face with your take on this spec

Ideas are welcome.
