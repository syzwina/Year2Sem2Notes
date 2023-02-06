[[COMP27112 - Table of Contents]]

# OpenGL
allows programmers to write software without having to worry about the hardware

# OpenGL API
- a specifiation of an API
- a set of functions to do 3D computer graphics
- used in mobile devices, industry, engineering, CAD, CGI, FX, research, games, education, - everywhere

# Portability
programmers writes code in favourite programming languages (C, C++, C#, Swift, Java, JS, etc.)
and the languages will make calls to the OpenGL library
and this will end up with code, that can run on any device (iOS, Android, macOS, Linux, Win, etc.)

# OpenGL evolution
![[../../images/Pasted image 20230202160123.png]]
## v1, v2
fixed pipeline - fixed functionality

![[../../images/Pasted image 20230202160238.png]]
the sequence of operations is fixed, the API can only change the parameter values

## v3+
programmable pipeline
extensible functionality - programmers can write micro-programs called **shaders**

![[../../images/Pasted image 20230202160338.png]]

can still do the 'fixed' pipeline

vertex shader program : decides the location of each vertex in my model, 3D-coordinates
fragment shader program : shades in the surfaces that we're dealing with

![[../../images/Pasted image 20230202160958.png]]

![[../../images/Pasted image 20230202161232.png]]

# OpenGL and Interaction

- OpenGL only generates pixels
- It doesn't handle interaction devices
- For interaction, we use GLUT library
![[../../images/Pasted image 20230202161517.png]]

# OpenGL Graphics
- 3D Graphics
	- points
	- lines
	- polygons
- Transformations (4-by-4 matrix)
	- scaling
	- shearing
	- rotation (x, y, z)
- Hidden Surface Removals
- Lighting and Shading
- Textures
- Modeling and Rendering
- Blending/Transparency

# Support Libraries

![[../../images/Pasted image 20230202162758.png]]

## GLU

GL Utility Library
- provides functions which wrap up lower level OpenGL graphics
	- curves
	- surfaces
	- cylinder
	- disc
	- quadrics
- Utility functions
	- viewing
	- textures
	- tesselation
- Command reference : https://www.opengl.org/sdk/docs/man/

## GLUT

GL Utility Toolkit
- Interaction 
	- mouse
	- keyboard
	- simple menu system
- Primitives
	- sphere, torus, cone, cube
	- tetra/octo/dodeca/icosa hedron
	- teapot

