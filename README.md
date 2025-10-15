# HW 4: *3D Stylization*

## Project Description:

https://github.com/user-attachments/assets/b6d872f6-20f0-4195-99d2-b400ef80cd08

### Extra Renders:

|<img src="Readme Assets//thinoutlines.png" width="650"/>|
|:--:|
|thin outlines|

|<img src="Readme Assets//nooutlines.png" width="650"/>|
|:--:|
|no outlines|

### 1. Concept Art:
I drew this concept art of Kirby in Procreate. I wanted painterly coloring and pencil-textured colored outlines.  <br>

<img src="Readme Assets//kirby.jpg" height="650"/>

### 2. Interesting Shaders:
I implemented multiple light support following this [tutorial](https://www.youtube.com/watch?v=1CJ-ZDSFsMM&list=PLEScZZttnDck7Mm_mnlHmLMfR3Q83xIGp&index=4).

I also implemented rim lighting. 

I used a simple noise function as a texture for my shader to make the edges between highlights/midtones/shadows less sharp. I also added a smoothness parameter to blend between the colors, giving it a more painterly effect. For the shadows, I used a custom texture I created in procreate using watercolor brushes to displace the edges of the shadow. I also made the edges of the shadow darker to mimic the effect of paint building up at the edges. 

|<img src="Readme Assets/interestingShadow.png" width="650"/>|
|:--:|
|rim lighting + textured toon shader|

For my special shader, I animated the vertices of the object by rotating it's positions and normals. I also added a glow effect by using bloom, emission, and enabling HDR. 

### Create a Scene:
In Maya, I modeled this scene of Kirby to closely resemble the concept art. 

<img src="Readme Assets//maya.png" width="650"/>

### Outlines:
I implemented Roberts Cross outlines based off of depth and normals. I used noise functions to make the outline resemble pencil and animated it over time with a step function. 

### Full Screen Post Process Effect:
I added a saturation parameter that changes the saturation of the scene. I also combined two noise functions to create a paper-like texture. 

<img src="Readme Assets//nosat.png" width="650"/>

### Interactivity
I implemented "Party Mode". When users press space, the rotation of the star increases and Kirby iterates through different colors.

https://github.com/user-attachments/assets/2d036e2e-f26e-4079-a4d5-f412d2c6a1c1
