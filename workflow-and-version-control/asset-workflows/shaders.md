# Shaders

Shaders must be made in-engine, as shaders from other sources (for example Blender shaders) are not supported in the final product. For each project, we use the PBR, or Physically Based Rendering, for our shader model. For this, PBR shaders will be made, with a few variants depending on the various textures that must be supported. For example, some of the PBR shaders support translucency, while others do not, for optimization reasons.

PBR Shaders, by default, support Albedo, Normals, Ambient Occlussion, Roughness and Metallic, through an Albedo texture, Normal texture, and ORM texture. Variants add support for Translucency through the Albedo's Alpha channel and Emission support through an Emission map.
