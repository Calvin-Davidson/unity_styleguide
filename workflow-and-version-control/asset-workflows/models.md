# Models

3D models are made in different 3D modeling programs depending on what kind of model is being produced. Hard surface models are made using Blender or Maya, while soft surface / sculpted models are made using ZBrush. All models are exported in FBX format, with a unit scale of 1 unit=1 meter, with X-forward, Z-right, Y-up orientation. Poly count limit should be up to 20.000 polygons depending on the model. Small props have a limit of 1.000, large props have a limit of 5.000, and characters have a limit of 20.000.

Once a model is made, it will be UV unwrapped and textured. Textures are made within Substance Painter, using the Texture workflow.

Once exported, the artist makes a new github branch to import the model. Once imported, the artist verifies the orientation and scale of the model, imports textures, creates materials, and applies the textures and materials. Once finished, this is uploaded to github and a pull request is made.
