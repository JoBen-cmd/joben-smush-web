# Introduction
*Excerpt paraphrased from Mario Kart 8 Lighting Guide*

## Baking Information
Unfamiliar with what you just read? Don’t worry, read these small sections that talk about everything you need to know in order to understand lighting in Super Smash Bros. Ultimate. Obviously, there’s more than just this, but what is written here is what’s necessary for you to make a stage look good.

### What exactly is "baking"?
Baking in 3D modeling is the process of storing information about a 3D mesh onto an image texture. Bakes can range from **normal baking**, which stores surface details and bumps as vector directions, to **shadow baking**, which gives a black and white texture where white is where the sun hits that part of the model and black is where it doesn’t, and this is one of them that we will be using.
The way to create these textures is by telling the software where to properly place what you’re baking, which is done by a process called **UV Mapping**. This is a process that projects the surface of a model into a 2D image that’s going to be our texture. This isn’t easy, however, because sometimes we don’t want some faces of the model to be where they are, so we have to **UV Unwrap** to get some of the job done. Not all, though, you still must put in a little bit of work.

### What is the point of baking?
The point is inherently for optimization purposes. Although the process is quite a pain, and half of the time it doesn’t work the way you want to, the performance boost it gives you is worth it.
In games, for example, shadows and other lighting are calculated through the engine. These are very intense and complicated calculations that the computer is making **per frame**, costing on performance. Bake maps help that by decreasing the calculation process a lot, and just giving how lighting is supposed to look in a specific area of the model, given by the texture, cutting out a huge chunk of the calculation process. Super Smash Bros. Ultimate takes advantage of this, and only calculates shadows from moving objects present in the stage, and not stuff that is static, making the game overall smoother.

### What types of bake maps does Super Smash Bros. Ultimate use?
Super Smash Bros. Ultimate uses two baked maps. These are:
* [**Baked Lighting**](https://scanmountgoat.github.io/Smush-Material-Research/textures/bakedlit/index.html): This is a colored map that is able to calculate the diffuse lighting and shadows on stages. A few examples of stages that use Baked Lighting are Battlefield, Kalos Pokémon League, & Fountain Of Dreams.
* [**Ambient Occlusion**](https://scanmountgoat.github.io/Smush-Material-Research/textures/prm/index.html#ambient-occlusion-blue): This is a black and white map that is used to approximate shadows. Although characters use the Blue channel for the PRM texture for ao maps, stages handle it differently as it occupies its own uv map so that way it occupies multiple meshes as its map1 texture might be different from one another. A few examples of stages that use Ambient Occlusion are Smashville and Gaur Plains.

#### Additional info
In this guide, I will be using **New Donk City’s Battlefield Form** as they contain Ambient Occlusion and Baked Lighting maps. With that, I’ll change the scene from Day time to sunset during the Music Festival.