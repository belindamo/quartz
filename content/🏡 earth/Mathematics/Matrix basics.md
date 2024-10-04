#concept-pamphlet 
#todo: I'm not certain of these definitions; this ties into my hesitations w.r.t. [[tensor]] definition

[[dot product]]



What is rank in machine learning?
?
Rank is the number of linearly independent rows or columns
<!--SR:!2024-11-05,99,296-->

What are a few uses of matrices?
?
- representing linear transformations
- handling multi-dimensional data
- solving systems of linear equations
- simplifying computational tasks in quantum mechanics.
<!--SR:!2025-04-05,195,290-->

Matrix A has dimensions a x b
Matrix B has dimensions c x d
What are the dimensions are Matrix AB, assuming dot product is a valid operation?
?
a x d
<!--SR:!2025-03-17,176,310-->



Matrix A has dimensions a x b
Matrix B has dimensions c x d
Which dimensions must be equal for AB to be a valid dot product?
?
b and c
<!--SR:!2025-04-15,205,310-->

(AT)T = >> A
<!--SR:!2024-10-03,66,270-->

(A + B)T = >> AT + BT
<!--SR:!2024-09-30,63,310-->

Transitive property: (P * Q)T = >> QT * PT
<!--SR:!2025-05-24,244,330-->

(AT)-1 = >> (A-1)T
<!--SR:!2024-10-07,15,315-->
<!--SR:!2024-08-09,4,294-->
<!--SR:!2024-08-06,4,294-->
<!--SR:!2024-08-05,4,294-->
<!--SR:!2024-08-05,4,292-->
<!--SR:!2024-08-03,4,292-->
<!--SR:!2024-08-02,4,292-->
<!--SR:!2024-08-02,4,293-->
<!--SR:!2024-08-16,18,308-->

Is the identity matrix diagonal? Is the zero matrix diagonal?
?
Yes because they both have all their off-diagonal elements as zero
<!--SR:!2025-05-06,226,330-->


Trace of matrix (tr(A))
??
![[Screenshot 2024-06-19 at 3.15.01 PM.png]]
in other words, it is the sum of matrix A's diagonal elements
<!--SR:!2024-08-19,14,290!2024-09-04,59,310-->


![[Screenshot 2024-06-19 at 3.15.30 PM.png]] >> ad - bc
<!--SR:!2024-08-20,22,270-->


Visualize the zero matrix >> Matrix of all 0s
<!--SR:!2024-10-08,71,310-->

Visualize the identity matrix >> Square matrix that is all 0s except on the diagonal. The diagonal is all 1s.
<!--SR:!2024-08-31,55,310-->

Visualize a symmetric matrix >> If you fold it over the diagonal like origami, it's the same
<!--SR:!2024-08-27,51,310-->

Determinant of matrix A (explanation only)
?
Scalar used to calculate the inverse of matrix A
![[IMG_0097.jpeg]]
![[Screenshot 2024-06-19 at 4.16.05 PM.png]]
<!--SR:!2024-08-22,24,190-->

Inverse matrix A^-1 where A is m x n will always be dimensions >> m=n. Square
<!--SR:!2024-08-11,10,270-->

A-1 * A = >> A * A-1 = I
<!--SR:!2024-10-12,75,277-->

(aA)-1 = >> a-1A-1
<!--SR:!2024-08-14,13,270-->

(AT)-1 = >> (A-1)T

(AB)-1 = >> B-1A-1
<!--SR:!2024-09-03,36,257-->





what does it mean for two vectors to be orthogonal, equation-wise?
?
The condition for two vectors x and y to be orthogonal in an n-dimensional space is defined by the dot product equation:
**x⋅y=0**
or xTy = 0
This equation means that the sum of the products of their corresponding components is zero. Explicitly, if x=(x1,x2,…,xn) and y=(y1,y2,…,yn), then:
x1y1+x2y2+…+xnyn=0
This condition must be satisfied for x and y to be orthogonal.
<!--SR:!2024-08-28,30,236-->

In the context of matrix manipulation, how might the dot product of two vectors a and b be represented? >> aTb ; this results in a scalar which is the dot product
<!--SR:!2024-08-11,10,270-->


Are vectors by default considered column or row vectors? >> column
<!--SR:!2024-08-14,38,296-->


### References
1. https://solutionhacker.com/cheatsheet-matrix/