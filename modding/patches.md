---
title: Patches
description: How to create custom patches.
published: true
date: 2024-06-22T21:03:06.709Z
tags: runtime
editor: markdown
dateCreated: 2024-05-22T20:00:56.528Z
---

## Creating a New Patch
Once you have followed the instructions to create a Staged Mod folder (see [quick-create](/modding/quick-create)), there will now exist a GroundBranch/Patches folder inside the Staged Mod folder:

<figure>
<img src="/images/patches/patches_patchfolder.jpg" width="60%" alt="Screenshot"/>
<figcaption>Location of the Patches folder</figcaption>
</figure>

Inside this folder, you can create a subfolder corresponding to the category of patch you are adding. This can be an existing category (e.g. Morale) or a new one:

<figure>
<img src="/images/patches/patches_patchtype.jpg" width="60%" alt="Screenshot"/>
<figcaption>Specifying a patch category</figcaption>
</figure>

You then place your new patch files inside this folder (the patch image files being created according to the specification below):

<figure>
<img src="/images/patches/patches_thepatch.jpg" width="60%" alt="Screenshot"/>
<figcaption>The patch itself</figcaption>
</figure>

All that remains now is to create the mod using the Quick Create system mentioned above.

## Patch Image File Specification

Ground Branch patches are a fixed size and aspect ratio (512x256 pixels) and a fixed filetype (.png). Patches that do not conform to these requirements will not be displayed. **The alpha channel is ignored** (if present), due to technical limitations involved in rendering the patches on both head and body. That is to say that patches cannot have any transparency.

Please note that although patch textures are saved with a 2:1 aspect ratio, they are displayed at 1.65:1 aspect ratio in-game. Therefore, if you want your source material to be rendered at the correct aspect ratio in-game (for example to keep circles circular), you will need to adjust the aspect ratio by a factor of 1.65:2 (i.e. 0.825) before saving.

The patch author name should be placed in parentheses at the start of the file name. Spaces should be replaced with underscore characters (\_).

A default normal map is used to display patches, unless a second image file is present, with the same name as the first but with a "\_N" suffix. The standard Unreal Engine 4 normal map format should be used. This is an example of a combination of a patch image file and its corresponding normal map image:

<figure>
<img src="/images/patches/patches_mainandnormal.jpg" width="40%" alt="Screenshot"/>
<figcaption>A patch image and its corresponding normal map</figcaption>
</figure>

The creation of normal maps is outside the scope of this document, but there exist many programs which will generate an estimated normal map based on an arbitrary source image, for example. Better results will be obtained by generating the source image and normal map in the same process, for example using custom patch generator scripts in Substance 3D and suchlike.

To summarise the requirements:

* Create a 512x256 PNG file: `(Author)Name.png`. Spaces should be replaced with underscore (`_`).
* Optionaly create a 512x256 PNG file containing the normal map: `(Author)Name_N.png`
* Put the file(s) into `Documents/GroundBranch/StagedMod/GroundBranch/Patches/<CATEGORY>/`.
* `<CATEGORY>` can be one of the existing ones ("BloodType", "Country", "Morale", "Role") or you can define a new category.
