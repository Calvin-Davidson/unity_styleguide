## Very large assets

This can be seen as a pseudo-exception to 2.6.
There are certain asset types that have a huge volume of related files where each asset has a unique purpose. The two most common are Animation and Audio assets. If you find yourself having 15+ of these assets that belong together, they should be together.

For example, animations that are shared across multiple characters should lay in Characters/Common/Animations and may have sub-folders such as Locomotion or Cinematic.

> This does not apply to assets like textures and materials. It is common for a Rocks folder to have a large amount of textures if there are a large amount of rocks, however these textures are generally only related to a few specific rocks and should be named appropriately. Even if these textures are part of a Material Library.