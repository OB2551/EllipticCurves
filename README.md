# Elliptic Curves

This code is an implementation of the Schoof and SEA algorithm for counting points on elliptic curves over finite fields. Python was chosen for ease of implementation at the cost of performance. SEA starts slowing down past 128-bit primes.

EllipticCurve.py  contains an EllipticCurve class which requires a prime p, and integers A and B to initialise an instance of the class. 
An EllipticCurve object has the methods schoof() and sea() to count the number of points on the elliptic curve y^2=x^3+Ax+B over the field F_p.

EllipticCurve.py  has dependencies on the other files in this repository, except for the GUI.py and .png file.

Other packages used are in the implementation are standard python packages: itertools, math, random, functools and operator.
The gmpy2 package is also used to help speed up arithmetic and will need to be installed.
Example.py contains a few example computations.
![Untitled2](https://user-images.githubusercontent.com/67613774/200215308-df3f9062-c35b-41a2-a2cf-74ab13810e4e.png)

![Untitled](https://user-images.githubusercontent.com/67613774/200215314-c0a96679-cd48-4821-910c-4c162d25ce79.png)

The GUI.py file provides a basic gui to use the sea or schoof algorithm for point counting, where the user can specify the curve parameters p,A,B.
customtkinter and tkinter need to be installed for GUI.py to run.


Point counting is of interest in elliptic curve cryptography.
For an introduction to point counting on elliptic curves, see for example:
https://en.wikipedia.org/wiki/Counting_points_on_elliptic_curves
