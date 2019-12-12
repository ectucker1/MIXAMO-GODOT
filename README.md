# MIXAMO-GODOT
- Blender Version 2.80, 2.81 - Not tested with other versions.
- Batch-Imports Mixamo-Animations without (!) skin from Fbx.
- Renames the actions according to Fbx-Filename.
- Can Batch-Save individual animations as Blendfiles.
- Also can Batch-Export animations as ESCN-Files,
- using the Godot-Blender-Exportes (Has to be installed).
- Doesn't remove the 'MixamoRig:' prefix from the Bone-Names, yet.
- Can't yet pack animations in a single .blend/.escn
- Doesn't work with meshes currently, only bare armatures with animations.
- Can't join animations in a single file, yet.
- Only work's with Fbx-Files.
- X, Z locations get removed completely from the Hip-Bone (!)

How to use:
0. You might want to replace spaces in the filenames (optional)
1. To see printed warnings/errors logs, open Blender in Terminal
2. Open a new file in blender and save it in the directory, with
   the files you downloaded from Mixamo. Working-Directory.
   If the Blendfile contains objects (default-cube or a model, camera etc.),
   the script will backup the file.
2. Open the script in the Text-Editor.
3. Change the Option-Variables True/False, for what you need.
4. Run the Script, done.

When you've exported to .escn you can:

$ cd your-anim-folder/escn_out
$ godot -e

______________________________________________________________

replacing ' ' with '_' on linux-terminal:
for foo in *.fbx; do mv "$foo" `echo $foo | tr ' ' '_'` ; done
