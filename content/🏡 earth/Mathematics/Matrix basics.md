#concept-pamphlet 
#todo: I'm not certain of these definitions; this ties into my hesitations w.r.t. [[tensor]] definition

[[dot product]]


What is rank in machine learning?
[[SR/memory/63yGWaxZ.md|?]]
Rank is the number of linearly independent rows or columns


What are a few uses of matrices?
[[SR/memory/HSzGhAnM.md|?]]
- representing linear transformations
- handling multi-dimensional data
- solving systems of linear equations
- simplifying computational tasks in quantum mechanics.


Matrix A has dimensions a x b
Matrix B has dimensions c x d
What are the dimensions are Matrix AB, assuming dot product is a valid operation?
[[SR/memory/aY3CyTdN.md|?]]
a x d



Matrix A has dimensions a x b
Matrix B has dimensions c x d
Which dimensions must be equal for AB to be a valid dot product?
[[SR/memory/0xeOBE5u.md|?]]
b and c
(AT)T = >> A
<!--LEARN:U7pdEVtV-->


(A + B)T = [[SR/memory/ZHZnsoSd.md|>>]] AT + BT


Transitive property: (P * Q)T = [[SR/memory/GGmX5Ra7.md|>>]] QT * PT


(AT)-1 = [[SR/memory/ACYe4YbF.md|>>]] (A-1)T


Is the identity matrix diagonal? Is the zero matrix diagonal?
[[SR/memory/X1WscCIa.md|?]]
Yes because they both have all their off-diagonal elements as zero


Trace of matrix (tr(A))
??
![[Screenshot 2024-06-19 at 3.15.01 PM.png]]
in other words, it is the sum of matrix A's diagonal elements


![[Screenshot 2024-06-19 at 3.15.30 PM.png]] [[SR/memory/FXbRpEut.md|>>]] ad - bc



Visualize the zero matrix [[SR/memory/9G6W2Jl7.md|>>]] Matrix of all 0s


Visualize the identity matrix [[SR/memory/Vzub2EI0.md|>>]] Square matrix that is all 0s except on the diagonal. The diagonal is all 1s.


Visualize a symmetric matrix [[SR/memory/JGjveem1.md|>>]] If you fold it over the diagonal like origami, it's the same


Determinant of matrix A (explanation only)
[[SR/memory/lYUDxfN6.md|?]]
Scalar used to calculate the inverse of matrix A
![[IMG_0097.jpeg]]
![[Screenshot 2024-06-19 at 4.16.05 PM.png]]
Inverse matrix A^-1 where A is m x n will always be dimensions >> m=n. Square
<!--LEARN:OAUcU4eO-->


A-1 * A = [[SR/memory/uSZltFQ8.md|>>]] A * A-1 = I


(aA)-1 = [[SR/memory/6RPplSNM.md|>>]] a-1A-1


(AT)-1 = [[SR/memory/dK3rS6Cy.md|>>]] (A-1)T

(AB)-1 = [[SR/memory/VQlHYupn.md|>>]] B-1A-1






what does it mean for two vectors to be orthogonal, equation-wise?
[[SR/memory/hzEbvOf9.md|?]]
The condition for two vectors x and y to be orthogonal in an n-dimensional space is defined by the dot product equation:
**x⋅y=0**
or xTy = 0
This equation means that the sum of the products of their corresponding components is zero. Explicitly, if x=(x1,x2,…,xn) and y=(y1,y2,…,yn), then:
x1y1+x2y2+…+xnyn=0
This condition must be satisfied for x and y to be orthogonal.


In the context of matrix manipulation, how might the dot product of two vectors a and b be represented? [[SR/memory/UHoOdjmx.md|>>]] $a^Tb$ ; this results in a scalar which is the dot product



Are vectors by default considered column or row vectors? [[SR/memory/zm5iQ57I.md|>>]] column



### References
1. https://solutionhacker.com/cheatsheet-matrix/