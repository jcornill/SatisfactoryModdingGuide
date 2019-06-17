# Installing Satisfactory Mod Loader (SML)

First you need to get SML to be able to start to add mod to satisfactory or to create mod.

SML will create a "xinput1_3.dll" file that you need.

If you don't want to build the source code and just want it to load mod you can find this at https://ficsit.app/sml-releases but I suggest you to build it from source for theses that want to create new mods.

I will explain how to build it in the next chapter for people that already have the "xinput1_3.dll" file you can skip it.

## Building Satisfactory Mod Loader

SML is still in heavy development and it's better if you learn how to build it from the source file.

### Get source from github

First you need to install something to clone the repository on your computer the easiest one is github deskop available [here](https://desktop.github.com/).

After downloading github desktop you need to go on SML github [here](https://github.com/satisfactorymodding/SatisfactoryModLoader).

Here you can choose between Master branch (Stable version) or Development branch (Latest updated branch but not stable).

In my example I will use the Development branch.
![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/blob/master/GitHub_SMLDownload.png "GitHub_SMLDownload")

Then you can go back on github desktop.

You need to go in **File > Clone Repository...** and select URL tab at the top.

On this page paste the link you got from github in repository URL, choose where you want to place the SML source then click Clone.
![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/blob/master/GitHubDesktop_clone.png "GitHubDesktop_clone")

Wait a bit for the code to be downloaded on your computer.

Perfect you have the SML source code on your computer.

### Building SML with visual studio

Now you need to get visual studio if you don't have it.

It's better to use Visual studio 2017, you can find older version of visual studio [here](https://my.visualstudio.com/Downloads?q=visual%20studio%202017&wt.mc_id=o~msft~vscom~older-downloads). Be sure to be log in to have the download appear.

When you have visual studio you can open the file "**SatisfactoryModLoader.sln**" with visual studio.

In the solution you have 3 projects available
+ Detours
+ ExampleMod
+ SatisfactoryModLoader

Ignore "**Detours**" and "**ExampleMod**" for now and right click on "**SatisfactoryModLoader**".

A context menu appear here you just need to click "Build".

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/blob/master/visualStudio_Build.png "visualStudio_Build")

Now click on Output at the bottom and wait until you see "**Build: 2 succeeded**".

It mean everything is working fine.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/blob/master/VisualStudio_Output.png "VisualStudio_Output")

Now you just need to get the file nammed "**xinput1_3.dll**".

On my computer the file is generated in this folder "**D:\CodingTutorial\SatisfactoryModLoader\x64\Release**".

## Loading SML into Satisfactory

Now you have the "**xinput1_3.dll**".

You need to place this file in a specific folder.

The path for the folder is "**SatisfactoryEarlyAccess\FactoryGame\Binaries\Win64**" from where you installed your game by default the game is installed in "**C:\Program Files\Epic Games\**".

Place the "**xinput1_3.dll**" inside this folder next to "**FactoryGame-Win64-Shipping.exe**" file.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/blob/master/Xinput.png "Xinput")

Now you can launch Satisfactory like with Epic like you always do.

If a command windows appear that means everything work correctly.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/blob/master/Console.png "console")

Now you can install mod compatible with SML by directly dropping them inside the created mod folder "**SatisfactoryEarlyAccess\FactoryGame\Binaries\Win64\mods**" and relaunch the game.

## Conclusion


Sorry for any misstying error or english error D:

If you have any question, error or sugestion about this guide you can send me a PM on discord Kirthos#4493.

Thanks for reading my guide I will make mroe guide about how to mod satisfactory.
