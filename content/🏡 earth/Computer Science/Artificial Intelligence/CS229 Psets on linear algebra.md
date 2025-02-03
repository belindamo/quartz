#concept-pamphlet #class
#todo: weed out the ones I want to keep vs. not
# pset 0

![[Screenshot 2024-06-09 at 8.45.25 PM.png]]
[[SR/memory/Rfnjz5Tx.md|?]]
![[Screenshot 2024-06-09 at 8.45.33 PM.png]]



![[Screenshot 2024-06-09 at 8.45.49 PM.png]]
[[SR/memory/sax2DHaR.md|?]]
![[Screenshot 2024-06-09 at 8.46.03 PM.png]]


![[Screenshot 2024-06-09 at 8.46.18 PM.png]]
[[SR/memory/X6HuoDQA.md|?]]
![[Screenshot 2024-06-09 at 8.46.41 PM.png]]


what is an important rule of thumb to keep in mind with matrix multiplication?
[[SR/memory/JNABOHol.md|?]]
Always think about the dimensions of a given expression


what is a gradient a collection of? what are its dimensions wrt f(x) and x's dimensions? visualize it.
*dimension meaning more similar to rank
[[SR/memory/f9ASrux7.md|?]]
collection of all first order derivatives.
if
x is n by 1
F() is tensor A by B by C
then
grad ( F (x) ) is A by B by C by n


what is a hessian a collection of? visualize it
[[SR/memory/VWUvo72U.md|?]]
collection of all second order derivatives. 


![[Screenshot 2024-06-25 at 4.12.02 PM.png]]
![[Screenshot 2024-06-09 at 8.47.17 PM.png]]
hint: think of the dimensions of gradient and hessian, for f: Rn -> R. gradient is nx1. hessian is nxn symmetric matrix
[[SR/memory/LkuUouCo.md|?]]
![[Screenshot 2024-06-09 at 8.47.31 PM.png]]


![[Screenshot 2024-06-09 at 8.47.40 PM.png]]
[[SR/memory/hfh39Nx0.md|?]]
![[Screenshot 2024-06-09 at 8.48.10 PM.png]]
TOREVIEW: How is xTAx a possible matmul? 




![[Screenshot 2024-06-09 at 8.48.19 PM.png]]
[[SR/memory/Oy3YfRLb.md|?]]
![[Screenshot 2024-06-09 at 8.48.35 PM.png]]


![[Screenshot 2024-06-09 at 8.48.49 PM.png]]
[[SR/memory/4MMmlo7b.md|?]]
![[Screenshot 2024-06-09 at 8.48.54 PM.png]]
TOREVIEW - null space? x^tz = 0? doesn't x need to be 1xn in shape? isn't xx^t also rank 2?


![[Screenshot 2024-06-09 at 8.49.06 PM.png]]
[[SR/memory/GFiXxgCq.md|?]]
![[Screenshot 2024-06-09 at 8.49.11 PM.png]]
it uses the PSD property of A and applies it to BABT!



![[Screenshot 2024-06-09 at 8.49.25 PM.png]]
[[SR/memory/Evnq3eOY.md|?]]
![[Screenshot 2024-06-09 at 8.49.34 PM.png]]


![[Screenshot 2024-06-09 at 8.49.42 PM.png]]
[[SR/memory/UJDQukPV.md|?]]
![[Screenshot 2024-06-09 at 8.49.51 PM.png]]



![[Screenshot 2024-06-09 at 8.52.38 PM.png]]
[[SR/memory/qSwzcKvo.md|?]]
![[Screenshot 2024-06-09 at 9.17.17 PM.png]]






![[Screenshot 2024-06-09 at 8.53.40 PM.png]]
[[SR/memory/p4JcwA8z.md|?]]
![[Screenshot 2024-06-09 at 8.53.47 PM.png]]






![[Screenshot 2024-06-09 at 8.55.49 PM.png]]
[[SR/memory/6HJTOQ7R.md|?]]
![[Screenshot 2024-06-09 at 8.55.55 PM.png]]


What is **rank** in deep learning? What rank does a scalar have?
[[SR/memory/yKyPHD0p.md|?]]
The rank of a matrix is the maximum number of linearly independent rows or columns in the matrix. For a 2x2 matrix, the rank can be 0, 1, or 2.
- It's 0 if all elements are zero.
- It's 1 if the rows (or columns) are proportional to each other (i.e., one row or column is a multiple of the other).
- It's 2 if the rows (or columns) are linearly independent (i.e., one row or column is not a multiple of the other).
The rank gives the number of dimensions spanned by the vectors formed by the rows or columns of the matrix.
A scalar has a rank of 0. A vector has a rank of 1, and a matrix can have rank 0, 1, or 2


What is **null space** in linear algebra?
[[SR/memory/vJhTy3wV.md|?]]
A null space (or kernel) of a matrix is the set of all vectors that, when multiplied by the matrix, result in a zero vector. In other words, if A is a matrix, the null space of A consists of all vectors x such that Ax = 0.