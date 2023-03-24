# Gitflow

To keep work efficent and organized, we use a dedicated workflow for anything we work on. This workflow combines the asset creation workflows, as well as the import pipeline and naming conventions.

### Creating an asset

When starting work on a new asset it is important to first get your local copy of the project up to date with the online copy. This is done through Github Desktop.

Once done, you must create a new branch as described in the Gitflow documentation.

Within the new branch, you can do the work needed to create the new asset, whether that's creating a texture in Substance Painter, or creating a model in Blender. Here you work in accordance with the corresponding Asset Workflow.

Once done with your work, it must be imported into Unity. Again, use the corresponding Asset Workflow to guide you on how to import your asset correctly.

After importing, go back to git to commit your changes. After that, push your changes.

With your work now being uploaded to the online copy, the last thing left is to merge it with the development copy of the project. This is done through a Pull Request. It is important to emphasize Request here, as it must be approved by another member of the team before the change gets merged.
