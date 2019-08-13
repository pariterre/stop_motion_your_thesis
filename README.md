# What is **stop_motion**
**stop_motion** is a LaTeX packtage that puts images on each pages so you can riffle them to get a nice stop motion effect!

# How to
The images must be assemble in a single folder with all the same names plus an index starting at 1 (e.g. *./images/image1.png*, *./images/image2.png*, *./images/image3.png*, etc)

To use it, after including the package, one must initialize **stop_motion** by using the ```\initializeStopMotion{path_to_images}{number_of_images}{x_position}{y_position}{size}``` command. 
Where ```x_position``` and ```y_position``` are the coordinates on the page (if twoside is defined, the even pages uses ```-x_position``` instead). 
The ```path_to_images``` is the relative or absolute path to the images, including the name of the images, but excluding the indices and extension (e.g. *./images/image*) . 
The ```number_of_images``` is the maximum index of image to draw before restarting to 1.

Afterwards, when they want to start the drawing of the images on the document, they must use the command ```\startStopMotion{starting_index}``` where ```starting_index``` default value is 1. 
To stop the stop motion, one can use the command ```\terminateStopMotion```. 
Please note that it is possible to restart the drawing, but default index will be again 1 and not the last one when the stop motion was terminated.

It is possible to rescale or reposition the image using the commands ```\setStopMotionSize{new_size}``` and ```\setStopMotionPosition{x_position}{y_position}```, which are pretty self-describing!

Enjoy stop motionning your documents!

Written by Pariterre on the 13th of August, 2019