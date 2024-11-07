# Multi-Mask Shader for ME
It's a shader mod, for HS2 / AIS MaterialEditor, based on [Multi-Masks.shader](https://github.com/Blatke/Multi-Masks.shader).

## How to Use
Download the **.zipmod** file for the latest version on the [Release](https://github.com/Blatke/Multi-Mask-Shader-for-ME/releases) Page, then drag and drop it into your **/mods/** folder to finish installation, or use KKManager to install this mod.

Use MaterialEditor to adjust the color and other parameters. 

## List of Properties
#### Mask2_ReplaceTintColor
AlbedoMask2 can replace the colors of tint and albedo, instead of blending them, with designated colors. But this option can independently decide whether the tint color is to be replaced or blended. When the value of this option is less than 1.0, the colors indicated by AlbedoMask2 will blend with the tint color instead of replacing it, so there is only the colors on the albedo map are replaced byAlbedo Mask2.

For instance, we add a folder in the scene with shifting its shader to Blake/Multi-Masks, and importing a texture of grid into its Albedo:

![AI_2024-11-07-19-27-25-332](https://github.com/user-attachments/assets/eabf7d57-266e-4607-b51f-640dd2837b5c)

We then change its Tint Color to, let us say, deep Cyan (0,1,0.8214285). It shows clearly the effect by blending the albedo texture with the tint.

![AI_2024-11-07-19-29-14-953](https://github.com/user-attachments/assets/da870277-b8cb-419d-86fd-3dfed1f180e9)

We assign AlbedoMask2 to a white image. Since AlbedoMask2 replaces by default the colors of the albedo and the tint, the folder shows totally white color (and of course you can change this white color to another one by adjust Mask2_White).

![AI_2024-11-07-19-32-31-204](https://github.com/user-attachments/assets/01629ed1-9102-4a98-adb8-025bb7c2dc6c)

Reduce the value in Mask2_ReplaceTintColor, make it less than 1.0, then you can see the folder shows Cyan color without the albedo. It's because now the white color on Mask2 are blended with the tint, that is white (1,1,1) * deep cyan (0,1,0.8214285)
## About Me
Bl@ke

Front Page: http://www.blatke.cc

Discord Server: https://discord.gg/nc5pmnf8X3

QQ Chatgroup for Modders: 904857543
