# FOR INNER CORE DEVELOPERS
Inner Core is a new generation of Minecraft PE mod loaders, that allows to create big and complicated mods. Here you can find all required information, that will help you to start development. 

# Learning Inner Core.

Inner Core mods are writen in JavaScript and require deep understanding of this launguage and how OOP works. This website might help you https://javascript.info/

This project is still very young and have massive API at the same time, so documentation is in development and for now you can learn mostly by understanding open-source mods. So here are some great examples of them:
1. Industial Craft PE: https://github.com/MineExplorer/IndustrialCraft_2 
2. Forestry: https://github.com/DDShadowRU/IC_ForestryPE

Both of this mods are quite big and well-writen, so you can study without any problems while documentation is not out.

##### Debugging mods:
1. All errors are showed in dialog windows and writen in log (games/com.mojang/innercore/innercore.log)
2. If startup log contain any errors it will show full log in dialog window. Errors are highlighted with red.

# Building and Publishing Mods

Inner Core allows to compile JavaScript into Java bytecode to improve its performance, so this operation is highly recommended before publishing your mod. 

##### Compiling Mod:
1. Open Inner Core menu, find your mod and open debug menu (right button).
2. You will see words "build type: develop" and a big button, that will start compilation (If you will see, that build type is "release" and you sure, that your mod contains all required source code, it means, that you just put incorrect build type into you build.config file, so press the button and confirm and move to step 3).
3. Press it and confirm.
4. Compilation will take some time to process (1-10 mins depending on mod size).
5. After compilation you might check it successful and restart Inner Core, next navigate to debug menu and make sure status of all executables is "ok [bytecode]".

Mod installation files are used to install mod in one click, by simly opening file with Inner Core or hitting "Install" in mod browser.

##### Creating installation file:
1. Make sure your mod is running without errors (check executable status in debug menu).
2. Pack your mod folder in zip archive.
3. If you really dont want to share your code with anyone: compile mod before step 2, after step 2 remove all source code files from your archive, but make sure you have copy of all this files. **BYTECODE COULD NOT BE REVERSE-ENGINEERED BACK TO JAVASCRIPT!**
4. Make extension of your file ".icmod"
5. Move your mod initial folder somewhere from mods directory and test your installation file by simply opening it with Inner Core and hitting install.
**IMPORTANT**: keep name of your mod folder same though all updates!

##### Uploading to Mod Browser:
1. Create installation file
2. Register at mod browser website, if you havent done it: http://icmods.mineprogramming.org/
3. Go to and upload your mod: http://icmods.mineprogramming.org/mod_new.php
4. You can edit and update updloaded mod from your account page.
