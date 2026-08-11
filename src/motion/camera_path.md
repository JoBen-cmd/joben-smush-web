# Camera Path
Many stages, such as Prism Tower, Skyloft, & Northern Cave, have a camera animation that moves through different sections of the stage. The file can be found here:

```
stage/stage_id/normal/motion/camera/
```

> [!NOTE]
> At the time of writing, there is no way to add a camera path to a stage that doesn't already have one.

### Creating your own Camera Path

The quickest and easiest way to create your own is by using the [Smash Ultimate Blender](https://github.com/ssbucarlos/smash-ultimate-blender/releases) plugin.

1. Import stage assets to Blender
2. Add a Camera (**Shift + A > Search "Camera"**), then select the Camera.
3. Press N, then click the `Ultimate` tab. Under `Animation Importer`, import the `.nuanmb` file and select the camera path.
4. You should now be able to preview and edit the stage camera files in Blender freely! 
5. Once you are ready to export, click on the camera, then go to `Animation Exporter` and export `.nuanmb`.

Since the Blender plugin automatically assumes that when you export the animation, it was a character victory screen, we'll need to fix that.
1. Install [ssbh_lib](https://github.com/ultimate-research/ssbh_lib/releases) and extract the contents.
2. Drag the `.nuanmb` file to `ssbh_data_json` and you should now have a JSON format. 
3. Open the JSON animation file and search for `gya_camera`. Change the name to `camera_stage`.
4. Save the JSON file and drag the JSON file to `ssbh_data_json`. You should now have an animation file that is a camera path for stages. Make sure that the file is named properly!

> [!NOTE]
> Some stages such as Wuhu Island also contains stage material animation data. If your stage mod requires material animations to the camera path, you'll need to create a separate `.nuanmb` file and combine the two files together  with ssbh_data_json.