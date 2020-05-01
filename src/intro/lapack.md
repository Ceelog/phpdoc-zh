LAPACK is written in Fortran 90 and provides routines for solving
systems of simultaneous linear equations, least-squares solutions of
linear systems of equations, eigenvalue problems, and singular value
problems. This extension wraps the LAPACKE C bindings to allow access to
several processes exposed by the library. Most functions work with
arrays of arrays, representing rectangular matrices in row major order -
so a two by two matrix \[1 2; 3 4\] would be array(array(1, 2), array(3,
4))
