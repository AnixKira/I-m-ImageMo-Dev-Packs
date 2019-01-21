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
