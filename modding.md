---
title: Modding
description: Modding Homepage
published: true
date: 2024-06-23T15:18:09.749Z
tags: 
editor: markdown
dateCreated: 2023-07-20T13:07:51.217Z
---

There are two main types of modding in Ground Branch: **non-asset based** (Quick Create) and **asset based** (Mod Kit / SDK), which are described in more detail below.

*The term 'asset' has a particular meaning within the Unreal Engine 4. Any file which is viewable within the Unreal Engine content browser is an 'asset'. With some limited exceptions (e.g. map files, .umap), Unreal Engine assets all have the .uasset file extension.*

## Non-Asset Based Mods (Quick Create)

Non-asset based mods are manually assembled by the modder within a 'staged mod' folder, and are packaged and uploaded within the game via the Modding->Quick Create menu.

With the exception of Mission files, non-asset files are readable and editable using external software, and often originate outside the game or SDK. Examples of non-asset files include patch images, game mode scripts, localisation files, kit files of various kinds, and so on. A Non-asset based mod may typically include several different types of files: for example, a game mode mod may additionally include missions for that game mode, localisation for the game mode, and custom AI kits.

The Quick Create system allows non-asset based mods to be made simply and quickly, and without having to download or use the Ground Branch Mod Kit / SDK.

-   List of non-asset file types
-   [Quick Create menu](/modding/quick-create)

### Game mode mods
-   Game mode modding overview
-   [Ground Branch Mission Editor guide](/modding/mission-editor)
-   [Ground Branch Lua Library guide](/modding/Lua-API)

### Patch mods
-   [Patch modding overview](/modding/patches)

## Asset Based Mods (Mod Kit / SDK)

The Ground Branch Mod Kit or SDK ("Software Development Kit") is used to create more advanced mods combining native Unreal Engine 4 elements such as textures, materials, static meshes, skeletal meshes, sounds, and so on.

Asset based mods are created, packaged and uploaded within the Mod Kit / SDK, which is downloadable as a separate program from the Epic launcher / store (@needs link when live). The SDK includes the base systems from Ground Branch but none of the maps and assets. Placeholder meshes are provided, for example for weapons, to allow you to access standard animations and sounds and suchlike.

-   [Creating a mod](/modding/sdk/creating-a-mod)
-   [Content types](/modding/sdk/content-types)
-   [Packaging a mod](/modding/sdk/packaging-a-mod)
-   [Uploading a mod](/modding/sdk/uploading-a-mod)
-   [Creating custom sounds with Wwise](/modding/sdk/Wwise)

The SDK was first released with Ground Branch version 1034. In this version, we are focusing on weapon mods only.

-   [Making an example weapon mod](/modding/sdk/making-an-example-mod)