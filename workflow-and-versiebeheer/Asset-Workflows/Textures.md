# Textures



* They are a power of two (For example, 512 x 512 or 256 x 1024).
* Use Texture Atlases wherever possible.
* It is better to resize the texture in Photoshop then to use Unity’s compression options when the in game texture resolution is already known. This reduces the file size and import time of the texture into Unity.
* When working with a high-resolution source PSD outside your Unity project use the same name for both the high-resolution and the imported Unity file. This allows quick iteration when swapping between the 2 textures.

More information for importing textures can be found here: https://docs.unity3d.com/Manual/ImportingTextures.html

Textures requiring the use of a Alpha channel should follow this guide: https://docs.unity3d.com/Manual/HOWTO-alphamaps.html
