#concept-pamphlet 
#todo: I'm not certain of these definitions; this ties into my hesitations w.r.t. [[tensor]] definition

[[dot product]]


What is rank in machine learning?
?
Rank is the number of linearly independent rows or columns
<!--LEARN:5joOcv6x-->

What are a few uses of matrices?
?
- representing linear transformations
- handling multi-dimensional data
- solving systems of linear equations
- simplifying computational tasks in quantum mechanics.
<!--LEARN:ySkzHrVf-->

Matrix A has dimensions a x b
Matrix B has dimensions c x d
What are the dimensions are Matrix AB, assuming dot product is a valid operation?
?
a x d
<!--LEARN:OkCIJrMT-->


Matrix A has dimensions a x b
Matrix B has dimensions c x d
Which dimensions must be equal for AB to be a valid dot product?
?
b and c
(AT)T = >> A
<!--LEARN:TeWwccjz-->

(A + B)T = >> AT + BT
<!--LEARN:5cCGDoBq-->

Transitive property: (P * Q)T = >> QT * PT
<!--LEARN:05Mbbh52-->

(AT)-1 = >> (A-1)T
<!--LEARN:siCnXvJq-->

Is the identity matrix diagonal? Is the zero matrix diagonal?
?
Yes because they both have all their off-diagonal elements as zero
<!--LEARN:DuxGOTll-->

Trace of matrix (tr(A))
??
![[Screenshot 2024-06-19 at 3.15.01 PM.png]]
in other words, it is the sum of matrix A's diagonal elements


![[Screenshot 2024-06-19 at 3.15.30 PM.png]] >> ad - bc
<!--LEARN:6kLIz1Fn-->


Visualize the zero matrix >> Matrix of all 0s
<!--LEARN:t5YTRbmN-->

Visualize the identity matrix >> Square matrix that is all 0s except on the diagonal. The diagonal is all 1s.
<!--LEARN:4pQ67vdB-->

Visualize a symmetric matrix >> If you fold it over the diagonal like origami, it's the same
<!--LEARN:EmJUwd77-->

Determinant of matrix A (explanation only)
?
Scalar used to calculate the inverse of matrix A
![[IMG_0097.jpeg]]
![[Screenshot 2024-06-19 at 4.16.05 PM.png]]
Inverse matrix A^-1 where A is m x n will always be dimensions >> m=n. Square
<!--LEARN:FeXhzZO5-->

A-1 * A = >> A * A-1 = I
<!--LEARN:NYM7RUD9-->

(aA)-1 = >> a-1A-1
<!--LEARN:iaUamhNP-->

(AT)-1 = >> (A-1)T
<!--LEARN:n63O5zOC-->
(AB)-1 = >> B-1A-1
<!--LEARN:CjFEyEed-->





what does it mean for two vectors to be orthogonal, equation-wise?
?
The condition for two vectors x and y to be orthogonal in an n-dimensional space is defined by the dot product equation:
**x⋅y=0**
or xTy = 0
This equation means that the sum of the products of their corresponding components is zero. Explicitly, if x=(x1,x2,…,xn) and y=(y1,y2,…,yn), then:
x1y1+x2y2+…+xnyn=0
This condition must be satisfied for x and y to be orthogonal.
<!--LEARN:G3hTv27n-->

In the context of matrix manipulation, how might the dot product of two vectors a and b be represented? >> $a^Tb$ ; this results in a scalar which is the dot product
<!--LEARN:UywgIYkv-->


Are vectors by default considered column or row vectors? >> column
<!--LEARN:SXEVUeHS-->


### References
1. https://solutionhacker.com/cheatsheet-matrix/