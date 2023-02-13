## Hierarchy strucutre

Next to the project’s folder, there’s also scene hierarchy. As before, we’ll present you a template. You can adjust it to your needs. Use named empty game objects as scene folders.

<pre>
Debug
Managers
PersistentSystems
UI
Cameras
Lights
World
    Terrain
    Props
Gameplay
	Actors
	Items
</pre>


- All empty objects should be located at 0,0,0 with default rotation and scale.
- For empty objects that are only containers for scripts, use “@” as prefix – e.g. @Cheats