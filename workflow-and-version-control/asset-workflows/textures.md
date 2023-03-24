# Textures

Textures are made using Substance Painter and Photoshop. When creating a texture, a default canvas is used with some basic restrictions on texture size. All texture resolutions should be a power of two (For example, 512 x 512 or 256 x 1024), with preferrably equal length and width for the texture. Where possible, please make sure to set these resolutions in the texture editing program so it does not have to be adjusted in game engine. Textures should never use the alpha channel, unless it is a color/albedo/diffuse texture that also requires the alpha channel for transparency/opacity.

In the case of 2D animations, we make use of Texture Atlasses. These are spritesheets made in the texture editing program instead of the game engine.

When exporting a texture or 2D animation, please export in PNG, though JPEG is also allowed. Name the exported file in accordance to the asset naming convention, so that the name is immediately correct upon import in game engine.

More information for importing textures can be found here: https://docs.unity3d.com/Manual/ImportingTextures.html

Textures requiring the use of a Alpha channel should follow this guide: https://docs.unity3d.com/Manual/HOWTO-alphamaps.html
