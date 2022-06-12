# Eigennodes-of-fractal-structure
Finding vibration eigennodes (Laplacian for an arbitrary shape, here a Koch fractal)

Created on Fri Feb 18 19:02:36 2022
@author: fredr

Multiple methods are tested to try out performance, only a couple are included here per step. The best performance functions are informed.

CODE PURPOSE:
    Find eigennodes (Laplacian) for arbitrary shape (here a Koch fractal)
This code performs the following:
    1    In order to generate a 2D squate koch fractal (file fractal_generator.py):
         There are two alternative methods, but both follow the same general steps
    1.1  Generates a 2D ("square") Koch fractal to a desired depth as a list of points that draws out the fractal
    1.2  Generates an empty lattice
    1.3  Superimpose the fractal on this lattice
    
    2   "Flag" the fractal. That is to distinguish between interior, exterior and boundary points (file flagg_lattic.py).
        There are two alternative methods, one using a flood fill algorithm and one using matplotlib Path.
        
    3   Generate Laplacian on matrix form for the fractal using the flagged lattice. 
        This is a finite difference method, that only takes nearest neighbours into account. Scipy scarse matrix
        (file Laplace_generator.py)
    
    4   Find eigenvalues from the laplacian using scipy built in function. These are eigennodes of the fractal structure
        (file Laplace_generator.py)
