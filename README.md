# Symbolic Fourier-Motzkin elimination

This library can be used to [project a
polyhedron](https://scaron.info/teaching/projecting-polytopes.html) using
[Fourier-Motzkin
elimination](https://en.wikipedia.org/wiki/Fourier–Motzkin_elimination) with
the two Imbert acceleration theorems. It is implemented in Python using
[SymPy](http://www.sympy.org/en/index.html) for symbolic computations and
multiprocessing to leverage the high degree of parallelization achievable with
this method.

## Trying out variable eliminations

This library is mainly a *graphical tool* to help a human user explore various
variable-elimination schemes to project a polyhedral cone given in symbolic
form. The user can explore the directed acyclic graph of variable-elimination
sequences, adding if-then-else nodes to the graph when desired. 

## Example

We used Fourier-Motzkin elimination to [derive the frictional wrench cone of
surface contacts](https://scaron.info/research/icra-2015.html) used in robotics
to alleviate computations caused by redundant contact-point models. The
step-by-step example ``wrench_cone.py`` derives automatically the calculations
from the Appendix of this paper. You can start from there for a first contact
with the GUI.

## Related libraries

For better performance on numerical rather than symbolic systems, you can use
the [double description
method](https://scaron.info/teaching/projecting-polytopes.html#double-description-method).
A number of libraries implement this algorithm, or similarly vertex enumeration
or convex hull algorithms:

- [cdd](https://www.inf.ethz.ch/personal/fukudak/cdd_home/index.html) (C) or [pycddlib](https://github.com/mcmtroffaes/pycddlib) (Python)
- [lrs](http://cgm.cs.mcgill.ca/~avis/C/lrs.html)
- [panda](http://comopt.ifi.uni-heidelberg.de/software/PANDA/)
- [pypoman](https://github.com/stephane-caron/pypoman)
- [ppl](http://bugseng.com/products/ppl/) (C++) or [pyparma](https://github.com/haudren/pyparma) (Python)
- [qhull](http://qhull.org/)
