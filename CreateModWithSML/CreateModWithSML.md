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

