# Gitflow

{% embed url="https://user-images.githubusercontent.com/34209869/219022095-46cc4503-76dc-40da-89e6-e58e6f592773.PNG" %}

To keep work efficent and organized, we use a dedicated workflow for anything we work on. This workflow combines the asset creation workflows, as well as the import pipeline and naming conventions.

### Creating an asset

When starting work on a new asset it is important to first get your local copy of the project up to date with the online copy. This is done through Github Desktop.

Once done, you must create a new branch as described in the Gitflow documentation.

Within the new branch, you can do the work needed to create the new asset, whether that's creating a texture in Substance Painter, or creating a model in Blender. Here you work in accordance with the corresponding Asset Workflow.

Once done with your work, it must be imported into Unity. Again, use the corresponding Asset Workflow to guide you on how to import your asset correctly.

After importing, go back to git to commit your changes. After that, push your changes.

With your work now being uploaded to the online copy, the last thing left is to merge it with the development copy of the project. This is done through a Pull Request. It is important to emphasize Request here, as it must be approved by another member of the team before the change gets merged.

### Branch types

#### Main

Main is the branch where finished products are put onto. This means that each version released on main is bug-free, and completely functional. As such, you cannot work directly in main.

#### Develop

Develop is the branch where any finished and verified work is put onto. This means that work-in-progress versions are available here. This also means you cannot work directly in develop.

#### Feature

Feature branches are used when working on specific feature's. after finishing this feature it's merged in develop after which this branch can be deleted.

#### Hotfix

Hotfix branches are for quick fixes, where there is a breaking bug in develop you can use a hotfix branch to quickly find the issue and fix it. a hotfix branch is still checked trough a pull-request

### Branch naming

Branch naming is relatively simple. It is made out of the type of branch, a slash, and then the name of the branch. For example, feature/importprojectfiles is a feature branch where project files are imported. asset/wolf would be an asset import branch where you are importing a wolf 3D model. Branch names are always lowercase.

![](<../.gitbook/assets/image (1).png>)

### Creating a new branch

To make a new branch, simply open Github Desktop. Then, press the "current branch" button at the top. There will be a popup, where you can select which branch you are working in. Select develop. Then, press the current branch button again, and press the new branch button. Select Develop as the base branch and give it an appropiate name. Github Desktop will now switch to that new branch, and allow you to publish it to github with the button next to the current branch button.

{% embed url="https://user-images.githubusercontent.com/53999981/226842411-020499a7-a475-478a-9150-3748f794d34a.png" %}

### Commiting changes

When your work is finished, github will list the changes you made. In the bottom left, you can give your changes a title, and a description. Please add a clear description of what is \[ADDED], \[CHANGED] or \[REMOVED]. After making the title and description, click the commit button in the bottom left. After that, press the push button at the top to upload to github.

{% embed url="https://user-images.githubusercontent.com/34209869/219022298-86de8e01-0310-445f-a58d-634e135179c2.PNG" %}

### Creating pull requests

After pushing, open github via your browser. In the repository, there should be a popup that mentions that the branch you just pushed has recent changes, and you should make a pull request for it. Press the create pull request button, which redirects you to the pull request page. At the top there is a compare option with two drop down menus. In the left menu, select develop. In the right menu, select the branch you just pushed. After that, it checks whether it is able to merge, and after that you can press the create merge request button. Once it is created, you should ask a teammate to check and merge it.

{% embed url="https://user-images.githubusercontent.com/34209869/219022335-b3707cc6-5da8-49dd-98c0-27c43cd17c7a.PNG" %}

### Pulling changes

Receiving changes is very easy. Simply switch to the branch you want to receive changes of, and press the fetch origin button. It will update and tell how many changes it can pull, and then you click pull.



