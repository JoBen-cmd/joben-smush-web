# Optimizations

### Textures
After importing all of the assets, you are also able to lower the filesize more by changing the Output Format with Ultimate Tex. Here’s what I recommend choosing depending on the texture name:

* _col (Albedo) - BC1RgbaUnormSrgb or BC3RgbaUnormSrgb if the texture contains alpha.
* _nor (Normal) - BC1RgbaUnorm
* _prm (PBR)- BC1RgbaUnorm
* _emi (Emissive)- BC1RgbaUnormSrgb
* _ao or _gao (Anbeint Occlusion) - BC1RgbaUnormSrgb
* _lit (Baked Lighting) - BC7RgbaUnormSrgb

From the <img src="/images/blender_icn/blender_icon_outliner_data_light.svg" style="vertical-align: middle; height: 1.2em;" alt="Stage_2 Preview"> section

### Futher Optimizations
If you are looking into making further optimizations, you can also remove vertices that aren’t present in the scene when playing the stage or use a different shader that has a lower shader complexity.

To view an object's shader complexity in SSBH editor, go to Menu > Render Settings. In the Debug Shading section, change the Debug Mode from Shaded to ShaderComplexity in the dropdown menu. If you selected the correct option, it should give you funky vibrant visuals. Yellow means that it's the most intensive while a dark blue-purple color means that it's very low in shader complexity. If there’s a background object that has a high shader complexity, consider choosing a lower complex shader if you are still facing performance problems.

![Shader Complexity](images/Shader_Complexity_Calendar.png)

> [!TIP] 
>The Debug Mode is also very useful for checking if your baked lighting or ambient occlusion texture are being applied properly amongst other things. To preview these textures in isolation, go to the Textures section and select Texture3 (Ambient Occlusion) or Texture9 (Baked Lighting). This should easily give you a preview of the baked maps.
