# Stage UI

## Stage Preview

![Stage Select Preview](images/Smash_Ultimate_Stage_Selection_Screen.png)

The Stage user interface in Smash Ultimate has many components that you should keep in mind if you were to modify the files. Here's some of the key components that you should keep in mind:

| UI Element | Preview | Description |
| :--- | :--- | :--- |
| **stage_0** | ![Stage_0 Preview](images/stage_0_Demon_Dojo.png) | Series Logo (The series icon found on the top right of the stage preview) |
| **stage_1** | ![Stage_1 Preview](images/stage_1_Demon_Dojo.png) | Small Portrait (The icon when you hover over a stage in the stage select) |
| **stage_2** | ![Stage_2 Preview](images/stage_2_Demon_Dojo.png) | Normal Portrait |
| **stage_3** | ![Stage_3 Preview](images/stage_3_Demon_Dojo.png) | Omega Portrait |
| **stage_4** | ![Stage_4 Preview](images/stage_4_Demon_Dojo.png) | Battlefield Portrait |
| **nam_stg1** | ![Stage Name Preview](images/nam_stg1_Demon_Dojo.png) | Stage Name. You can find this in `ui/message/msg_name.msbt` |

You can find these stage files located at 
```
ui/replace/stage/stage_# - for normal stages
ui/replace_patch/stage/stage_# - for dlc stages
```

## Stage Parameters

You can also change the appearance and/or sereis icon of a stage slot by modifying the `ui_stage_db.prc` file located here:

```
ui/param/database/ui_stage_db.prc
```

This prc file allows you to modify the stage order, decide whether it uses the album selector like Battlefield and Final Destination, and more. Here's the list of what each param does.

| Param | Description |
|---------|---------|
| ui_stage_id     | ID for stage UI.     |
| ui_series_id    | ID for the stage's sereies mark icon.      |
| stage_place_id    | ID for where      |
| secret_stage_place_id     | def     |
| secret_command_id     | def     |
| secret_command_id_joycon     | def     |
| bgm_set_id     | def     |
| dlc_chara_id     | The DLC character ID    |
| name_id    | Name of the stage. This is stored in the nam_stg1 msbt section     |
| save_no     | The save number for the game's save data.     |
| can_select     | Allows the stage to be selected on the stage select.     |
| can_demo     | Allows the stage to appear in demo mode on the title screen.     |
| is_8player_stage     | Allows a stage to appear in the fourth rotation of the demo mode in the tile screen (note that the demo player count can only be six).     |
| is_usable_flag     | Determines if it can be used in VR mode.     |
| is_usable_amiibo     | Determines if it can be selectable on amiibo Journey.     |
| bgm_selector     | Determines whether it uses the album selector when selcting music on a stage.     |
| is_dlc     | Determines if the stage is DLC in the game.     |
| is_patch     | Determines if the stage is patched in the game.     |
| disp_order     | Display order on the stage select.     |
| bgm_setting_no     | Playlist ordreing for a stage's music playlist.     |