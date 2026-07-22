# Creating Stage UI

> [!NOTE]
> Screenshots may be more accurate on Emulator than Console.

## Stage_0

The series logo has the same color channels that's commonly used for greyscaled Smash Ultimate UI textures. The red channel is the greyscaled texture that is also applied in the blue and green channel. The green channel is used as a alpha channel.

The process is fairly simple. I reccomend using [Swtich Toolbox](https://github.com/KillzXGaming/Switch-Toolbox/releases) as it will make changing the channels far easier. I'll be using [Photopea](https://www.photopea.com/) since everyone can use it. Any other 2D image editing software should work too. We'll be using the original Legend of Zelda logo from [Zelda Wiki](https://zelda.fandom.com/wiki/The_Legend_of_Zelda) as an example.

1. Create a new project and set the dimensions to **160w x 80h**.
2. Open and place the image and readjust it to where you can see the series icon.
3. Create a greyscaled image by **Image > Adjustments > Black & White**. Press ok and then export it as a .png or .dds (BC7Srgb for .dds will be best since that's the highest image quality).
> [!TIP]
> Depending on the series icon, you may want to invert the series icon. In order to do so, click on the layer of the iamge and press `ctrl + I`. That should give you a inverted image that will flip from black to white or vise versa.
> You may also want add an outer glow effect like other `stage_0` previews.
4. Open Switch Toolbox, then open the `stage_0_stageid.bntx` file that you plan to replace.
5. Right click on the image and replace the image with yours.
6. Click the `Channels` section and click on the Alpha Channel. Right Click > Export Channel.
7. Close the window and re-open the stage_0.bntx file again (Sorry for the inconvienience, but you should be fine after this).
8. Go back to the `Channels` section and on the green channel, Right Click > Replace Channel and select the alpha channel that you previously exported.
9. Do the same steps like above but now for the red channel. Make sure to select the greyscaled texture.


Just a reminder:

Properties Channels:
* Red Channel: **Red**
* Green Channel: **Red**
* Blue Channel: **Red**
* Alpha Channel: **Green**

Channels:
* RGBA - Resulting Image from the 3 channels listed below (Don't worry if it looks weird)
* Red - **Greyscaled Image**
* Green - **Alpha Channel**
* Blue - **Black (Unused)**
* Alpha - **White (Unused)**

If everything looks good, you can now to to File > Save As and place it to your desired location. 

## Stage_1 & Stage_2

1. Blank the Mario model to remove fighters from the stage. You can do this by copying the `model.numdlb` file:

```
stage/battlefield/normal/model/bg_efftcts_set/model.numdlb
```
into:
```
fighter/mario/model/body/c00/model.numdlb
fighter/mario/model/body/c01/model.numdlb
```
2. Since the small and normal portraits can't be easily replicated due the positions and fov changing depending on the stage, there's two options to choose from.
* Go into Vs. mode and have Player 1 & 2 select the first 2 Mario costumes and in Camera mode, eyeball it until it looks like it's close to vanilla.
* Do a similar setup [here](http://localhost:3000/cli/creating_stage_ui.html#setting-up-the-screenshot) and adjust the params till it's close to vanilla.

2. For stage_2, create a new project with dimensions **512w x 256h**. For stage_1, use **108w x 90h**.
3. Place and adjust the screenshot as needed.
4. **Image > Adjustments > Exposure:** set Gamma Correction to 0.45.
5. Export as .png or .dds.
6. In Ultimate Tex: File > Add Files..., open your image(s).
7. Make sure to select Output settings:
      - Output Type: **Nutexb**
      - Output Format: **Color (Linear) + Alpha**
      - Mipmaps: **Disabled**
      - Compression: **Slow**
8. Choose `Select Folder...` to select your disired location then click on the `Export` button.

## Stage_3 & Stage_4

Omega and Battlefield previews are fairly consistent for all stages in Smash Ultimate, so we can get a close proximation in order to create our own:

#### Setting up the screenshot
   1. Blank the Mario model (see Stage_1 & Stage_2 step).
   2. Update the .stprm file to change fixed camera values. You can use any prc Editor but the one shown below are the values that needs to be changed:
```
# pyprc script from ThatNintendoNerd
from pyprc import *
import sys

file = param(sys.argv[1])

file[hash("fixed_camera_fov")].value = 52
file[hash("fixed_camera_center_x")].value = 0
file[hash("fixed_camera_center_y")].value = 42
file[hash("fixed_camera_center_z")].value = 200
file[hash("fixed_camera_horizontal_angle")].value = 0
file[hash("fixed_camera_vertical_angle")].value = -5

file.save(sys.argv[1])
```
   3. Go to Training mode and select the first two Mario skins for Player 1 & CPU.
   4. In the pause menu, set Camera to "Fixed" (press Y or ◀ on single joy-con).
   5. Exit the pause menu and take a screenshot.

#### Image Editor
1. Create a new project with dimensions **512w x 256h**.
2. Place the screenshot, resize to **938 pixels horizontally** using Bicubic interpolation, then center it on the canvas.
3. **Image > Adjustments > Exposure:** set Gamma Correction to 0.45.
4. Export as .png or .dds.
5. In Ultimate Tex: File > Add Files..., open your image(s).
6. Make sure to select Output settings:
      - Output Type: **Nutexb**
      - Output Format: **Color (Linear) + Alpha**
      - Mipmaps: **Disabled**
      - Compression: **Slow**
7. Choose `Select Folder...` to select your disired location then click on the `Export` button.