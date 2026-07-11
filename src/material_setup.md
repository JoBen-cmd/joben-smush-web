# Material Setup

Setting up the material is fairly easy thanks to the Smash Ultimate Blender Plugin. To convert a mesh to a Smash Ultimate material, go to the  tab and select Convert Blender Material under the Ultimate Material Data section. 

Insert Image

This will allow you to make importing/exporting the models far easier for testing. Although this has been converted to a Smash Ultimate shader, it uses the standard PRM Opaque, which is a shader that shouldn’t be used for stages, as it's a very complex shader that should only be used for fighters.

Here’s a few Shader Labels I recommend using:

Baked Lighting:
Mainstage/Platforms
Background
Ambient Occlusion:
Mainstage/Platforms
Background
Simple Shaders (Meshes that won’t be Baked)
Mainstage/Platforms
Background
SFX_PBS_0000000009088240_opaque
A shader that only features a col texture but also receives shadows and stage lighting.


>[!TIP]
> There are so many to choose from, so don’t stress out if it's not the perfect shader! You can use SSBH Editor to open various stage models in Smash and open the material (model.numatb) file to see what contents you want to have on your shader. There’s also a built-in Shader Finder under **Material > Find Shader** in the material editor if you are looking for something very specific. More info about material parameters can be found [**here**](https://github.com/ScanMountGoat/Smush-Material-Research/blob/master/Material%20Parameters.md).