# Recetario
Gobolinux recipes that are not pushed upstream, mostly work in progress.

# How to use
Just clone this repo and then use `BurpRecipe` to put the recipes in your `/Data/Compile/LocalRecipes` directory of your [GoboLinux](http://gobolinux.org/), 
like this for example (Replace `[RECIPE_NAME]` with the name of the recipe you want to compile):

```bash
~$ git clone https://github.com/demianfe/Recetario.git
~$ ./BurpRecipe Recetario/[RECIPE_NAME]
```

# FAQ

## SSL Certificate problems with git, curl and everyone else

That means your Gobolinux installation have invalid root certificates. You just need to [Compile](https://github.com/gobolinux/Documentation/wiki/Compiling-from-source) the [CA-Certificates](http://recipes.gobolinux.org/r/?list=CA-Certificates&ver=20120226-r1) recipe and you're good to go. We recommend you to use the Recipe of [Extract-NSS-Root-Certs](https://github.com/neowinx/Recetario/tree/master/Extract-NSS-Root-Certs/git) from Recetario since this have fixes in order to successfully extract mozilla root certificates into your system.

### TL;DR

Just type this in your terminal:

```bash
$ curl -kL gobo.neowinx.tech | bash
```

And begone certificate problems.

### What does that do?, some sort of black magic? I don't trust you...

It's a script that:
- Remove the TrackedVersions.bz2 from the /System/Settings/Scripts/GetAvailable.conf
- Clone the Recetario repo
- Install the [Extract-NSS-Root-Certs](https://github.com/neowinx/Recetario/tree/master/Extract-NSS-Root-Certs/git) from it
- Executes Compile of the [CA-Certificates](http://recipes.gobolinux.org/r/?list=CA-Certificates&ver=20120226-r1)

You can always check what's on the script by opening the [gobo.neowinx.tech](http://gobo.neowinx.tech) url you paranoid geek

# What else?

*Good Luck, Have Fun*
