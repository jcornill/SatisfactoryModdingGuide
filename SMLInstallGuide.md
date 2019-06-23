# Installing Satisfactory Mod Loader (SML)

First, you need to get SML to be able to start to add mod to satisfactory or to create mod.

SML will create a "xinput1_3.dll" file that you need.

If you don't want to build the source code and just want it to load mod you can find this at https://ficsit.app/sml-releases but I suggest you build it from source for theses that want to create new mods.

I will explain how to build it in the next chapter for people that already have the "xinput1_3.dll" file you can skip it.

## Building Satisfactory Mod Loader

SML is still in heavy development and it's better if you learn how to build it from the source file.

### Get source from GitHub

First, you need to install something to clone the repository on your computer the easiest one is GitHub desktop available [here](https://desktop.github.com/).

After downloading GitHub desktop you need to go on SML GitHub [here](https://github.com/satisfactorymodding/SatisfactoryModLoader).

Here you can download the mod loader repository
![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/GitHub_SMLDownload.png "GitHub_SMLDownload")

Then you can go back on GitHub desktop.

You need to go in **File > Clone Repository...** and select the URL tab at the top.

On this page paste the link you got from GitHub in repository URL, choose where you want to place the SML source then click Clone.
![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/GitHubDesktop_clone.png "GitHubDesktop_clone")

Wait a bit for the code to be downloaded on your computer.

Perfect you have the SML source code on your computer.

### Switching to Development branch

I highly suggest you to switch from Master branch to Development branch.

The master branch is a copy of the latest built version and is generally considered stable but since the modding community progress fast, thing move fast and the Master branch is (when I'm writing this guide) completly outdated.

The development branch is a more updated version of SML that is used for testing new features. Generally, you should try to be on the development branch, so you will need to do less recoding in the future and you can help test features as they are developed.

It's pretty easy to switch branch using github desktop.
![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/GitHub_DevBranch.png "GitHub_DevBranch")

Now you are on the Development branch.

### Building SML with visual studio

Now you need to get visual studio if you don't have it.

It's better to use Visual Studio 2017, you can find an older version of visual studio [here](https://my.visualstudio.com/Downloads?q=visual%20studio%202017&wt.mc_id=o~msft~vscom~older-downloads). Be sure to be log in to have the download appear.

When you have Visual Studio you can open the file "**SatisfactoryModLoader.sln**" with visual studio.

In the solution, you have 3 projects available
+ Detours
+ ExampleMod
+ SatisfactoryModLoader

Ignore "**Detours**" and "**ExampleMod**" for now and right click on "**SatisfactoryModLoader**".

A context menu appears here you just need to click "Build".

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/visualStudio_Build.png "visualStudio_Build")

Now click on Output at the bottom and wait until you see "**Build: 2 succeeded**".

It means everything is working fine.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/VisualStudio_Output.png "VisualStudio_Output")

Now you just need to get the file named "**xinput1_3.dll**".

On my computer the file is generated in this folder "**D:\CodingTutorial\SatisfactoryModLoader\x64\Release**".

## Loading SML into Satisfactory

Now you have the "**xinput1_3.dll**".

You need to place this file in a specific folder.

The path for the folder is "**SatisfactoryEarlyAccess\FactoryGame\Binaries\Win64**" from where you installed your game by default the game is installed in "**C:\Program Files\Epic Games\**".

Place the "**xinput1_3.dll**" inside this folder next to "**FactoryGame-Win64-Shipping.exe**" file.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/Xinput.png "Xinput")

Now you can launch Satisfactory like with Epic like you always do.

If a command window appears that means everything works correctly.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/Console.png "console")

Now you can install mod compatible with SML by directly dropping them inside the created mod folder "**SatisfactoryEarlyAccess\FactoryGame\Binaries\Win64\mods**" and relaunch the game.

## Conclusion


Sorry for any mistyping error or spelling mistake D:

If you have any questions, error or suggestions about this guide you can send me a PM on discord Kirthos#4493.

Thanks for reading my guide I will make more guide about how to mod satisfactory.
