# Textures

* They are a power of two (For example, 512 x 512 or 256 x 1024). Depending on the asset, texture size should be limited to 512 for small props, 1k for large props, and 2k for characters.
* Use Texture Atlasses wherever possible.
* It is better to resize the texture in Photoshop then to use Unity’s compression options when the in game texture resolution is already known. This reduces the file size and import time of the texture into Unity.
* When working with a high-resolution source PSD outside your Unity project use the same name for both the high-resolution and the imported Unity file. This allows quick iteration when swapping between the 2 textures.
* Textures should only use the RGB channels where possible, especially on mask textures. Use alpha only where necessary.

Supported file formats are PNG and JPEG, though PNG is preferred.

More information for importing textures can be found here: https://docs.unity3d.com/Manual/ImportingTextures.html

Textures requiring the use of a Alpha channel should follow this guide: https://docs.unity3d.com/Manual/HOWTO-alphamaps.html
