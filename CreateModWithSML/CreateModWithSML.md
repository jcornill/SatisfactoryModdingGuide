# How to make your first mod using Satisfactory Mod Loader (SML)

## 1-Introduction

In this detaileld guide I will explain you step by step how to make a simple mod for satisfactory using SML. 

This guide explain how to make new command, sneding message in the chat and giving items

This guide nto explain how to add new machine/item/recipe to the game. This will be in another guide.

## 2-Requirements

This guide require:
+ Knowledge in C++, I will not explain how work the programing language.
+ The satisfactory mod loader installed and working (check my [other guide](https://ficsit.app/guide/9ZYFESKroqiQgw) explaing how to install and compile SML)
+ Visual Studio 2017

## 3-Building default Example mod

Before starting to make our own mod let's try to compile and make the example mod work without any modification.

Open Satisfactory Mod Loader solution. Here you can find 3 differents projects.
+ Detours
+ ExampleMod
+ SatisfactoryModLoader

In this guide we will ignore Detours and SatisfactoryModLoader (you supposed to already have this build)

Open the ExampleMod project and open ExampleMod.cpp. This file is documented to help you making your first change to the mod.

You can ignore all FG_ files they are needed for your mod but don't try to modify them.

Don't change anything yet and build the exampleMod project to see if your mod loader is setup correctly.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/CreateModWithSML/Build_ExampleMod.png "GitHub_SMLDownload")

Like for the Satisfactory Mod Loader wait until you see "Build: 1 succeeded".

Now it's time to test the mod go, you need to move the mod .dll into the mods fodler inside your game directory.

The mod .dll is created inside the folder "**SatisfactoryModLoader\x64\Release**", search for "**ExampleMod.dll**" file.

And copy/move this file in the mods directory created by SML when you launch the game with SML installed located at "**Epic Games\SatisfactoryEarlyAccess\FactoryGame\Binaries\Win64\mods**".

To test if you mod work, create a new world or load an existing one then press the key 'G'. If everything work pressing the key will show a message in the console. You can test the "/kill" command that simply kill you.

Now we know everything is working correctly we can start making change to make our own mod.

## 4-Make a new command

In this chapter I explain you how to make a new command that print "Hello world" in the in game chat. If you go at line 49 you can find the KillPlayer method executed when you do the command. The comment available in the exampleMod file explain you how to add command. First you need to create a new method, the one we want to call when the player write our command.

So below the actual "killPlayer" method I've added my "helloWorld" method

```cpp
void helloWorld(Functions::CommandData data) 
{

}
```
SML implement a simple way to send a message in the chat using the player. First we need to create the string we will send in the chat. Satisfactory use FString when they need text. And FString is using wide char so you need to add the letter "L" before your text.
```cpp
void helloWorld(Functions::CommandData data) 
{
    SDK::FString* fString = &SDK::FString(L"Hello World");
}
```
Now we need a reference to the player that will send the message. ExampleMod come already with a reference to the player so you can just call the function using your variable player (contains reference to the player) and the fString we created above.
```cpp
void helloWorld(Functions::CommandData data) 
{
    SDK::FString* fString = &SDK::FString(L"Hello World");
    ::call<&AFGPlayerController::EnterChatMessage>(player, fString);
}
```
but if you try this code you will see it's not working. It's because SML use a custom FString class, you need to add a cast to make it work.
```cpp
void helloWorld(Functions::CommandData data) 
{
    SDK::FString* fString = &SDK::FString(L"Hello World");
    ::call<&AFGPlayerController::EnterChatMessage>(player, reinterpret_cast<FString*>(fString));
}
```
Now our command is ready to work but what command to type to execute this code ?

We need to explain to SML what chat command will trigger our method. We can do that around line 145.
Here you see the code that explain the kill command.

Below the kill command we just need to add our line to register our command.

```cpp
    Functions::registerCommand("hello", helloWorld);
```
Here "hello" is the command we will write in the chat and "helloWorld" is the reference to the method we created above.

Now we can compile the mod like we have done in chapter 3 and we can test it.

![alt text](https://github.com/jcornill/SatisfactoryModdingGuide/raw/master/CreateModWithSML/HelloWorld.png "HelloWorld")

It work as expected.
