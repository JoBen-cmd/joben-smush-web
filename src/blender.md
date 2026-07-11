# Blender

During Smash Ultimate's development, devs used Autodesk Maya as their primary 3D modeling software for stage assets and animation data for the game engine, along with Substance Painter to create textures. For our use case, we will use Blender not only because it is free, but also because the Smash Ultimate Blender plugin streamlines model importing and exporting in the long run.

This guide will focus on stages, from setting up the project scene, adjusting the materials, and finally creating your own baked lighting texture. As such, I will cover the full baking process for the baked lighting and ambient occlusion. I will also be using Blender 5.1. If you are planning on using a different version, it might not translate as well. I will assume that you are familiar with Ultimate’s textures and file structure. If not, click [here](https://scanmountgoat.github.io/Smush-Material-Research/introduction/index.html) for more information.

> [!CAUTION]
> This will NOT be a modelling guide. There’s a lot of guides online on how you can create your own models and so from here on out, I will assume that you have the models on hand. I advise you to look on YouTube on how to move around and familiarize yourself with Blender.


### Tools used in this guide:

#### Applications
- [Blender](https://www.blender.org/download/releases/5-1/)
- [SSBH Editor](https://github.com/ScanMountGoat/ssbh_editor/releases/)
- [Ultimate Tex](https://github.com/ScanMountGoat/ultimate_tex/releases/)

#### Blender Add-ons:
- [Smash Ultimate Blender](https://github.com/ssbucarlos/smash-ultimate-blender/releases/)
- [UV-Packer](https://www.uv-packer.com/blender/) (Not necessary but useful for cleaner uv `bake1` maps)

> [!TIP]
> Not sure how to install Blender add-ons? Click [here](https://www.youtube.com/watch?v=LzdoUTvAgXk).

## Huge Thanks
* Smash Ultiamte Material Research - For the tools and giving me a better understanding of Smash Ultimate's rendering process.
* [Mario Kart 8 Lighting Guide](https://docs.google.com/document/d/1TxgjOsM3FAJb-PnugwJeyd33MfTGPEtHCFolKVaIGHs/edit?usp=sharing) - Helped me out a lot with creating this guide.