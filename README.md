# ClassSing

## What's ClassSing?

`ClassSing` is a [MAGMA](http://magma.maths.usyd.edu.au/magma/) function that checks whether all singularities of a given projective algebraic curve are ADE singularities.

## Why ClassSing?

[MAGMA](http://magma.maths.usyd.edu.au/magma/) has a built-in function to check whether all singularities of a given _surface_ are of ADE type, but lacks a similar function for the case of algebraic curves. The `ClassSing`function fills this suprising gap.

## Usage

To use ClassSing, simply copy the content of classsing.txt into an open MAGMA session. Once the function is defined, you can use it as follows:

1. Fix the basefield to be the field of rational numbers.
`QQ:=Rationals();`

2. If some of the singular-point coordinates of the given curve contain irrational numbers, adjoin these irrationalities to the basefield. For example, if a:=sqrt(5) is such an irrationality, you can adjoin it to the basefield via
`F<a>:=ext<QQ|[Polynomial([-5,0,1])]>;`

3. Define the basering. Notice that the variables have to have the names x, y, and z.
`K<x,y,z>:=PolynomialRing(F,3);`

## License

`ClassSing`is released under the [GNU General Public License 3](http://www.gnu.org/licenses/gpl-3.0.html).

## Authors

Marco Besier, Dino Festi
