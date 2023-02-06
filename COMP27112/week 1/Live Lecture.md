don't spend more than a day on the courseworks
WebGl(made in JavaScript) is a wrapper for OpenGl(made in C)

# Point Processing Techniques
- increase brightness
- image negative
- isolate eggs in an image
	- if we look at the red values of the image, we'll see that the eggs has a higher red value
	- then we can do thresholding, if it's above a value, set it to white, if below a value set it to black
	- and then we can process somemore and find the eggs

# Applications
- medical imaging
- forensics
- geometrical transformations - moving the pixels around
	- tranformations
	- skew
	- scaling
	- radial
	- translational
- image calibration
	- there's some geometrical distortion
	- due to the lense
	- we can find out how much the image is being bent, and we can fix it
- image noise and noise reduction
	- if we take a picture at night without flash
	- the camera would try to compensate and boost the signals
	- and we end up w a noisy image
- edge operators
- edge detection
	- if it's a darker image next to a brighter image
- connected compoent analysis
	- after we found the edge
	- we fill the image to signify objects
	- label each objects w a different shade/id
- camera exposure
	- changes the size of the arpeture, how much light goes through
	- so that we can capture a good picture of a fast moving object
- image compression
	- jpeg compression
- the hough transform
	- looks at the edges
	- circle detection
- binary morphology - much  like the connected compoent analysis
	- opening, separate tadpoles
	- closing, get rid of eyes of the tadpoles
- 
