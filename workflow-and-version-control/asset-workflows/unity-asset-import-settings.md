Unity's [AssetPostprocessor](https://docs.unity3d.com/ScriptReference/AssetPostprocessor.html) lets you hook into the import pipeline and run scripts prior to or after importing assets. This allows you to enforce import settings when assets are first imported into the project. For example textures that end with _N can be marked as a Normal Map on import.

Example guide for Import Settings:

[https://github.com/justinwasilenko/Unity-AssetPostProcessor](https://github.com/justinwasilenko/Unity-AssetPostProcessor)