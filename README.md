# Cyobj

A python library for Wavefront .OBJ reading/writing

Why did we write yet another .obj reader/writer?

Many python libraries for .obj do not support 

* Texture coodinates
* Vertex normals
* Mixed quad/triangle
* Automatic generation of .mtl file when texture map exists
* Fast read/write

Therefore we wrote one ourselves that supports them all.

## Requirement

* NumPy
* Cython

## Install

`python setup.py build && python setup.py install`

## Running time

Compared to libigl-python-binding,

### Reading

Reads a large .obj (Armadillo) file with V/VT/VN attributes

* cython: 465.68751335144043 ms
* igl(C++): 1043.8106060028076 ms

### Writing

Writes an .obj file with V attributes

* cython: 252.14886665344238 ms
* igl(C++): 362.7943277359009 ms


