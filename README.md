<a href="https://gitlocalize.com/repo/4333"> <img src="https://gitlocalize.com/repo/4333/whole_project/badge.svg" /> </a>
<img src="https://travis-ci.org/bartzaalberg/alias.svg?branch=master" />

# Archived
This repository is not maintained anymore and will not be updated to Elementary OS 6.0. You have my blessing to create a fork and update the application to post publish it in Elementary 6.0 under your own name. 

# Alias
Simplify your commands

<p align="center">
    <a href="<p align="center">
    <a href="https://appcenter.elementary.io/com.github.bartzaalberg.alias">
        <img src="https://appcenter.elementary.io/badge.svg" alt="Get it on AppCenter">
    </a>
</p>

<p align="center">
    <img
    src="https://raw.githubusercontent.com/bartzaalberg/alias/master/screenshot.png" />
</p>

### alias for elementary OS

A tool to manage your bash aliases.

## Installation

First you will need to install elementary SDK

 `sudo apt install elementary-sdk`

### Dependencies

These dependencies must be present before building
 - `valac`
 - `gtk+-3.0`
 - `granite`

 You can install these on a Ubuntu-based system by executing this command:

 `sudo apt install valac libgtk-3-dev libgranite-dev`

### Building
```
meson build --prefix=/usr
cd build
ninja
```

### Installing
`sudo ninja install`

### Recompile the schema after installation
`sudo glib-compile-schemas /usr/share/glib-2.0/schemas`

### Update .pot file
Call the following command from the build folder:

`ninja com.github.bartzaalberg.alias-pot`

## FAQ

### Does the application work with ZSH?

ZSH is not supported out of the box. It is however possible to use the application with ZSH if you add the following lines to your `.zshrc` file.
```
if [ -f ~/.bash_aliases ]; then
    source ~/.bash_aliases
fi;
```
