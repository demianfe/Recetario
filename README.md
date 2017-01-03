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

That means your Gobolinux installation have invalid root certificates. You just need to [Compile](https://github.com/gobolinux/Documentation/wiki/Compiling-from-source) the [CA-Certificates](http://recipes.gobolinux.org/r/?list=CA-Certificates&ver=20120226-r1) recipe and you're good to go.

### TL;DR

Just type this in your terminal:

```bash
$ curl -kL gobo.neowinx.tech | bash
```

And begone certificate problems.

*Good Luck, Have Fun*
