#concept-pamphlet #class
#todo: weed out the ones I want to keep vs. not
# pset 0

![[Screenshot 2024-06-09 at 8.45.25 PM.png]]
?
![[Screenshot 2024-06-09 at 8.45.33 PM.png]]
<!--SR:!2024-10-06,76,270-->



![[Screenshot 2024-06-09 at 8.45.49 PM.png]]
?
![[Screenshot 2024-06-09 at 8.46.03 PM.png]]
<!--SR:!2024-10-25,58,190-->

![[Screenshot 2024-06-09 at 8.46.18 PM.png]]
?
![[Screenshot 2024-06-09 at 8.46.41 PM.png]]
<!--SR:!2024-12-17,132,270-->


what is an important rule of thumb to keep in mind with matrix multiplication?
?
Always think about the dimensions of a given expression
<!--SR:!2025-01-24,129,260-->

what is a gradient a collection of? what are its dimensions wrt f(x) and x's dimensions? visualize it.
*dimension meaning more similar to rank
?
collection of all first order derivatives.
if
x is n by 1
F() is tensor A by B by C
then
grad ( F (x) ) is A by B by C by n
<!--SR:!2024-10-28,61,220-->

what is a hessian a collection of? visualize it
?
collection of all second order derivatives.
<!--SR:!2024-11-19,83,240--> 


![[Screenshot 2024-06-25 at 4.12.02 PM.png]]
![[Screenshot 2024-06-09 at 8.47.17 PM.png]]
hint: think of the dimensions of gradient and hessian, for f: Rn -> R. gradient is nx1. hessian is nxn symmetric matrix
?
![[Screenshot 2024-06-09 at 8.47.31 PM.png]]
<!--SR:!2024-10-05,38,170-->


![[Screenshot 2024-06-09 at 8.47.40 PM.png]]
?
![[Screenshot 2024-06-09 at 8.48.10 PM.png]]
TOREVIEW: How is xTAx a possible matmul?
<!--SR:!2024-10-08,21,222--> 




![[Screenshot 2024-06-09 at 8.48.19 PM.png]]
?
![[Screenshot 2024-06-09 at 8.48.35 PM.png]]
<!--SR:!2024-11-22,66,230-->

![[Screenshot 2024-06-09 at 8.48.49 PM.png]]
?
![[Screenshot 2024-06-09 at 8.48.54 PM.png]]
TOREVIEW - null space? x^tz = 0? doesn't x need to be 1xn in shape? isn't xx^t also rank 2?
<!--SR:!2024-10-04,17,170-->


![[Screenshot 2024-06-09 at 8.49.06 PM.png]]
?
![[Screenshot 2024-06-09 at 8.49.11 PM.png]]
it uses the PSD property of A and applies it to BABT!
<!--SR:!2024-11-07,71,230-->



![[Screenshot 2024-06-09 at 8.49.25 PM.png]]
?
![[Screenshot 2024-06-09 at 8.49.34 PM.png]]
<!--SR:!2024-10-29,95,264-->


![[Screenshot 2024-06-09 at 8.49.42 PM.png]]
?
![[Screenshot 2024-06-09 at 8.49.51 PM.png]]
<!--SR:!2024-12-19,136,284-->



![[Screenshot 2024-06-09 at 8.52.38 PM.png]]
?
![[Screenshot 2024-06-09 at 9.17.17 PM.png]]
<!--SR:!2024-11-07,101,262-->






![[Screenshot 2024-06-09 at 8.53.40 PM.png]]
?
![[Screenshot 2024-06-09 at 8.53.47 PM.png]]
<!--SR:!2024-09-26,9,182-->






![[Screenshot 2024-06-09 at 8.55.49 PM.png]]
?
![[Screenshot 2024-06-09 at 8.55.55 PM.png]]
<!--SR:!2024-09-23,4,150-->

What is **rank** in deep learning? What rank does a scalar have?
?
The rank of a matrix is the maximum number of linearly independent rows or columns in the matrix. For a 2x2 matrix, the rank can be 0, 1, or 2.
- It's 0 if all elements are zero.
- It's 1 if the rows (or columns) are proportional to each other (i.e., one row or column is a multiple of the other).
- It's 2 if the rows (or columns) are linearly independent (i.e., one row or column is not a multiple of the other).
The rank gives the number of dimensions spanned by the vectors formed by the rows or columns of the matrix.
A scalar has a rank of 0. A vector has a rank of 1, and a matrix can have rank 0, 1, or 2
<!--SR:!2025-01-20,125,261-->


What is **null space** in linear algebra?
?
A null space (or kernel) of a matrix is the set of all vectors that, when multiplied by the matrix, result in a zero vector. In other words, if A is a matrix, the null space of A consists of all vectors x such that Ax = 0.
<!--SR:!2024-11-02,66,202-->