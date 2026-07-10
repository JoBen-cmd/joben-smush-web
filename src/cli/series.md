# Series Logo (stage_0)

The series logo has the same color channels that's often used for black/white Smash Ultimate UI textures. The red channel is the greyscaled texture that is also applied in the blue and green channel. The green channel is used as a alpha channel.

### Creating a series_0.bntx file

The process is fairly simple. I reccomend using [Swtich Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/releases) as it will make changing the channels far easier. I'll be using [Photopea](https://www.photopea.com/) since everyone can use it. Any other 2D image editing software should work too. We'll be using the original Legend of Zelda logo as an example.

1. Create a new project and set the dimentions to **160w x 80h**.
2. Open and place the image and readjust it to where you can see the series icon.
4. Create a greyscaled image by **Image > Adjustments > Black & White**. Press ok and then export it as a .png or .dds (BC7Srgb for .dds will be best since that's the highest image quality).
> [!TIP]
> Depending on the series icon, you may want to invert the series icon. In order to do so, click on the layer of the iamge and press `ctrl + I`. That should give you a inverted image that will flip from black to white or vise versa.
5. Open Switch Toolbox, then open the `stage_0_stageid.bntx` file that you plan to replace.
6. Right click on the image and replace the image with yours.
7. 