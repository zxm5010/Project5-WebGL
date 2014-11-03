-------------------------------------------------------------------------------
CIS565: Project 5: WebGL
-------------------------------------------------------------------------------
Fall 2014
-------------------------------------------------------------------------------
Due Monday 11/03/2014
-------------------------------------------------------------------------------

-------------------------------------------------------------------------------
NOTE:
-------------------------------------------------------------------------------
This project requires any graphics card with support for a modern OpenGL 
pipeline. Any AMD, NVIDIA, or Intel card from the past few years should work 
fine, and every machine in the SIG Lab and Moore 100 is capable of running 
this project.

This project also requires a WebGL capable browser. The project is known to 
have issues with Chrome on windows, but Firefox seems to run it fine.

-------------------------------------------------------------------------------
INTRODUCTION:
-------------------------------------------------------------------------------
In this project, you will get introduced to the world of GLSL in two parts: 
vertex shading and fragment shading. The first part of this project is the 
Image Processor, and the second part of this project is a Wave Vertex Shader.

In the first part of this project, you will implement a GLSL vertex shader as 
part of a WebGL demo. You will create a dynamic wave animation using code that 
runs entirely on the GPU.

In the second part of this project, you will implement a GLSL fragment shader
to render an interactive globe in WebGL. This will include texture blending,
bump mapping, specular masking, and adding a cloud layer to give your globe a 
uniquie feel.

-------------------------------------------------------------------------------
CONTENTS:
-------------------------------------------------------------------------------
The Project5 root directory contains the following subdirectories:
	
* js/ contains the javascript files, including external libraries, necessary.
* assets/ contains the textures that will be used in the second half of the
  assignment.
* resources/ contains the screenshots found in this readme file.

-------------------------------------------------------------------------------
PART 1 
-------------------------------------------------------------------------------

* A sin-wave based vertex shader:

![Example sin wave grid](https://github.com/zxm5010/Project5-WebGL/blob/gh-pages/renders/vertex_wave.jpg)


**Wave Of Your Choice**

* A wave that simulates generation of blocks or buildings, etc.

![Interesting Wave](https://github.com/zxm5010/Project5-WebGL/blob/gh-pages/renders/interesting_wave.jpg)

![Interesting Wave2](https://github.com/zxm5010/Project5-WebGL/blob/gh-pages/renders/interesting_wav2.jpg)

-------------------------------------------------------------------------------
PART 2 REQUIREMENTS:
-------------------------------------------------------------------------------

Features implemented:

* Bump mapped terrain
* Rim lighting to simulate atmosphere
* Night-time lights on the dark side of the globe
* Specular mapping
* Moving clouds

Extra freature implemented:

* Procedural water rendering and animation using Perlin noise 


Final Images:
![Final Image](https://github.com/zxm5010/Project5-WebGL/blob/gh-pages/renders/all_features.jpg)

![Final Image2](https://github.com/zxm5010/Project5-WebGL/blob/gh-pages/renders/image1.jpg)

Possible Improvement for water rendering:

In the project, I simply used Perlin noise for changing the color of the water texture. As the result, it doesn't look that real. To achieve the reality, Perlin noise should be used to change the normal of water and make a bump for it. Then, it should look more like waves. 

-------------------------------------------------------------------------------
PERFORMANCE EVALUATION
-------------------------------------------------------------------------------

According to stat.js. All the simulations can be run above 60 fps. The time consumption for each frame is about 10-20 ms. I tried to remove Perlin noise, and other stuff, such as cloud rendering, to see if there is any difference in performance. The result is pretty close to each other. When the program just started, there is a peak consumption, which is due to the texture reading and initialization. 

