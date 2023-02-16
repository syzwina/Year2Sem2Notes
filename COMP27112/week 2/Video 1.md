# Transformations
- vector and matrix representations
- homogeneous transformation
- composite transformation
- vector geometry

# 3D Cartesian coordinates
- origin is not necessarily fixed
- the axis is not necessarily fixed

so there are a few ways to use cartesian coordinates in 
computer graphics and image processing(if you tke computer vision next year)

![[../../images/Pasted image 20230210121303.png]]

	this is a Right-Handed coordinate system
if you arrange your thumb, 1st finger and 2nd finger at right angles
the 1st finger represents the x-axis
the 2nd finger represents the y-axis
the thumb represents the z-axis

in computer graphics, 
we have the x and y representing the horizontal plane, and the z going into the image plane

# Vectors

![[../../images/Pasted image 20230210121827.png]]

![[../../images/Pasted image 20230210121847.png]]

in computer graphics, we use column representation

# Geometrical Transformations

a cube is represented by the coordinates of it's vertices
a torus is represented by the coordinate of it's centre and the radius

to transform an object,
we have to apply transformations to wach of the vertices of the object

## Translate

![[../../images/Pasted image 20230210122205.png]]

## Scale

![[../../images/Pasted image 20230210122220.png]]

## Rotation

![[../../images/Pasted image 20230210122241.png]]

we want to rotate point P about the origin, by angle theta
IMPORTANT: anticlockwise - the positive direction of rotation

![[../../images/Pasted image 20230210122421.png]]

Rotation about a point

![[../../images/Pasted image 20230210122750.png]]

Rotation in 3D

![[../../images/Pasted image 20230210122810.png]]

![[../../images/Pasted image 20230210122932.png]]

Rotation in 3D about a vector = applies same principle to rotation in 2D about  point

![[../../images/Pasted image 20230210123028.png]]

![[../../images/Pasted image 20230210123042.png]]



