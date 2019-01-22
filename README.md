# I-m-ImageMo-Dev-Packs
This Repo is for dev tools, information and more, and packs to help you get started

Here we will include all the resoruce you will need to start using the Dev Mod, the dev mod is for testing out your own
ides, we are working on a tool that will create the dev dll's needed to run the dev mod, we will also in the future add
naked lua support for testing without having to complie all the time.

The dev mod option is found in About then holding the home button and right licking on the build from under the version
number this will actvate your dev DLL you will need to also know how we load the dlls

## Code
```Lua
__DevDLLLoad = package.loadlib("kOnLibDev.dll", "kOnOpen_Dev");
```

This is left over code from the Kingfisheranime days, the new version will have a different dll ext it will not use **.dll** it will use **.imod** and will use **iMod_load** as it's entry point rather then **kOnOpen_Dev**


The new version of the mod support will load right after the core so the modders will have more control over there mod, only one mod file will ever be supported as the mod file loaded is able to take control over part of the app there for braking other mods if there used the same namespace.

## Code
```Lua
 __iModLoader = package.loadlib("iModConnection.imod", "iMod_load");
```

Also right now the Dev Mod loads two late and loads the GUI before the options are set, this will also be changed in the future.
also in the future the mod mode will also have a *Naked* mode where you can test your mods before releasing them this would offer
you to load the file naked in .lua, reason we say this is not recommended for release versions is your end user can mess with code.
