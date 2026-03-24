(كتبت البحث بالإنجليزي عشان مشكلة الكتابة من اليمين للشمال)

## Determinants represented geometrically
<hr>

### prerequisites
* vectors
* i-hat and j-hat
* linear systems being represented in matrices and vectors
* linear transformations

<hr>

### vectors
let's consider vectors as column-matrices or row-matrices that we've learned before, except that they have special properties such as dot products (will be discussed later).

vectors typically look like this:

![image](https://i.postimg.cc/zfz8vHP6/Screenshot-20260323-224812.png "also included in addition")

and are represented geometrically like this:

![Screenshot-20260323-225904.png](https://i.postimg.cc/Y2Znb4Y4/Screenshot-20260323-225904.png)

In fact I think it looks like the one we learned in unit 4. Actually, operations are way too similar also.
lets consider vector v and w. to add them, we move the tail of vector w to the arrow-head of vector v, and then draw a new vector v + w that points to the result, as if we were getting the displacement:

![image](https://i.postimg.cc/tTY0nKGy/Screenshot-20260323-230619.png) 

you could also imagine increasing vector v's (X,Y) positions by vector w's (X,Y) positions move by move and not in one go, and then draw a new vector v + w that points to  the result.

now let's say we wanted to multiply vectors. To start, lets represent our vectors v and w algebrically.

![image](https://i.postimg.cc/nLc3SqzJ/Screenshot-20260323-235328.png)

we can see that the entries of vector v are v<sub>1</sub>, and v<sub>2</sub>, and vector w's entries as w<sub>1</sub> and w<sub>2</sub>. To multiply both vectors, we multiply each entry corresponding to the other in both vectors. like this: x = v<sub>1</sub> * w<sub>1</sub> , y = v<sub>2</sub> * w<sub>2</sub>.

then we add x and y together to produce one numeric value.

z = x + y

This operation is known as dot product(-ion). the resulted value (z) from the addition (x + y) is called "the dot product". let's have an example:

![image](https://i.postimg.cc/fLWk9TBH/Screenshot-20260324-000634.png)

here we multipled 4 *(corresponding entry in vector v)* by -1 *(corresponding entry in vector w)*, and 2 by 2, then added both of them to get the dot product, 0.
<hr>


### i-hat and j-hat
unit vectors can be represented geometrically as i-hat and j-hat.
i-hat corresponds to vector (1,0) pointing to the x-axis. j-hat corresponds to (0,1) pointing to the y-axis. together they are called the basis vectors.

![image](https://i.postimg.cc/sXCq6vtP/Screenshot-20260324-001632.png)

if they were to change, for example i-hat moves one unit forward in the x-axis, the coordinate plane will also move one unit forward, becoming (2,0). so the plane feels extended. An indicator can be the plane's sub-squares. They will transform into a rectangle with a length of 2 units. When the basis vector change their coordinates, the grid lines of the coordinate plane will also move in their direction. This behavior is known as a linear transformation.

### Linear Transformations

A linear transformation must have its grid lines evenly spaced and parrallel to each other.

here's a video showing a linear transformation when moving i-hat to (1,-2) and j-hat to (3,0). Look what happens to the grid lines and how the sub-squares are transformed into a parallelogram.

https://github.com/user-attachments/assets/e32be8ca-4484-4957-aab7-82bc262c51c0

You may have already noticed that other vectors on the plane also move with the transformation. And that is true, as a Linear transformation tends to shift everything into one direction, depending on how the basis vectors change.

A linear transformation that is _not evenly spaced_ or _not parallel_ cannot be considered linear.

In the following example, could you tell which one is considered a linear transformation?

![image](https://3b1b-posts.us-east-1.linodeobjects.com/content/lessons/2016/linear-transformations/figures/what-makes-a-transformation-linear/question1.png)

>[!NOTE]
>The answer is C. As the grid lines are parallel and evenly-spaced.

>[!IMPORTANT]
>Matrix multiplication can be considered as a function to linearly transform the basis vectors. In which you multiply the basis vectors by any matrix/vector to give a specific transformation.
>
>for example:
>
![image](https://www.3blue1brown.com/content/lessons/2016/linear-transformations/figures/examples/ShearMatrix.svg)

this is a shear transformation. For now, you dont have to know what that means or how it looks like, but the idea here is that we multiply the basis vectors by the shear vector (x,y) to make the matrix turn into [(1,0),(1,1)]. which gives a shear-looking coordinate plane, where j-hat moves one unit to the right. Keep in mind that the first column of the matrix represents i-hat, and the second column represents j-hat.

### linear systems being represented in matrix equations and vector equations

<img width="202" height="93" alt="image" src="https://github.com/user-attachments/assets/ebd64451-2441-4eec-9b29-a1b277ee1107" />

such linear systems can be represented as matrices, where you insert their coefficients as entries.

<img width="194" height="82" alt="image" src="https://github.com/user-attachments/assets/187a29aa-6251-467a-b039-42e9d67fd6f9" />

but they could also be represented as matrix equations. Matrix equations are simply a linear system that is written in the form ``Ax = b``, where ``A`` is a matrix containing the coefficients, ``x`` is a vector containing the unknowns, and ``b`` is the result as a vector. Take this linear system as an example:

<img width="726" height="407" alt="image" src="https://github.com/user-attachments/assets/c5ad3b4e-1f93-411b-a665-941e8edecb60" />

with the help of linear combinations (which consists of 2 operations: multiplying by a scalar and adding) we can reform (1) as a series of linear combinations that form a vector equation (2), and then into a single matrix equation (3).

>[!NOTE]
>geometrically, we would represent ``A`` as a transformation to the vector containing (x,y) to give us our result (4,1). The video up could be a demonstration to this. Before the transformation, we had our basis vectors (1,0) , (0,1) as

