# ChoiceScript Syntax for Sublime

❕ **Version 1.0.0**

This is a custom syntax highlighter with custom autocompletes and optional color scheme created for [ChoiceScript](https://www.choiceofgames.com/about-us/). Developed to make reading and writing ChoiceScript code quicker and easier, with the included "ChoiceScript" color scheme it targets specific aspects of code to differentiate via color.

It is compatible with **Sublime 3** and **4**.

#### ⚠️ This is NOT an IDE like CSIDE.
It does not include a copy of ChoiceScript. It cannot run QuickTest or RandomTest. It does not check for bugs or errors. It does not include a word count. You **must** have a copy of [ChoiceScript](https://github.com/dfabulich/choicescript) (or [CSIDE](https://github.com/ChoicescriptIDE/main/releases)) on your computer or use the [web version of CSIDE](https://choicescriptide.github.io/web/) to run your game.

## 📖 Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Color Scheme](#color-scheme)
- [Screenshots](#screenshots)
- [Autocomplete Commands](#autocomplete-commands)
- [Editing and Customization](#editing-and-customization)
- [Disclaimer](#disclaimer)

## Features
- Custom syntax highlighting for the ChoiceScript language.
- Full support for multireplace and stat charts.
- Custom color scheme for enhanced syntax highlighting.
- Autocomplete commands to quickly create common lines of code (page breaks, line breaks, choices, if/else statements, stat charts, comments, etc).
- Spell check for plain text and text for choice options and text in multireplace.
- Word wrap automatically enabled, tabs to indent conversion (for CSIDE compatiblity) enabled, auto match disabled (to keep from matching quotes).

## Installation
The ChoiceScript syntax can be installed one of two ways.

### 🛠 Manual Installation
1. ddd

### 📦 Package Control (recommended)
1. ddd

## Color Scheme
Included is an optional color scheme designed for the syntax. Since it was created for this specific syntax definition, it is able to target more specific parts of code to allow for enhanced highlighting.

It recognizes:

- Variables vs plain text in multireplace.
- Variables vs operators in `*if/*else` statements, including `and` and `or`.
- Image file names in `*image` and `*text_image` commands.
- When an `*if/else` or `*selectable_if` is immediately followed by an `#option` without a line break.
- When a value is set to `true` vs `false` in `*create`, `*temp`, and `*set`.
- When a `*page_break` is followed by plain text.
- Commands vs variables vs plain text in `*stat_chart`.

Some of this does carry over rather well to other color schemes, but the custom color scheme was designed alongside the syntax highlighter to highlight with greater thoroughness and accuracy for ChoiceScript.

## Screenshots
Below are screenshots of the syntax, with and without the color scheme, featuring scene files from Choice of Games' [Choice of the Dragon](https://www.choiceofgames.com/dragon/) and my own project.

### 💎 Without the Color Scheme
*Click for full size.*

Sublime's Mariana | One Dark Gravity
----------------- | -----------------
<img alt="Mariana" src="https://user-images.githubusercontent.com/33694865/120052569-900e2d00-bfeb-11eb-92a5-dc4f8bb19fc1.png">|<img alt="One Dark Gravity" src="https://user-images.githubusercontent.com/33694865/120052570-90a6c380-bfeb-11eb-9266-7f58db04fd67.png">
<img alt="Mariana2" src="https://user-images.githubusercontent.com/33694865/120053103-09a71a80-bfee-11eb-8b89-9b5739e65af3.png">|<img alt="One Dark Gravity2" src="https://user-images.githubusercontent.com/33694865/120053104-0a3fb100-bfee-11eb-8565-c4dac24893af.png">

Solarized Light | Solarized Dark
--------------- | --------------
<img alt="Solarized Light" src="https://user-images.githubusercontent.com/33694865/120052820-d1530c80-bfec-11eb-864b-dfffa547d5c3.png">|<img alt="Solarized Dark" src="https://user-images.githubusercontent.com/33694865/120052823-d1eba300-bfec-11eb-9491-ae385cf6c554.png">
<img alt="Solarized Light2" src="https://user-images.githubusercontent.com/33694865/120053108-0b70de00-bfee-11eb-9da1-b84ff6e1a6be.png">|<img alt="Solarized Dark2" src="https://user-images.githubusercontent.com/33694865/120053106-0ad84780-bfee-11eb-99b8-fcc7edf2a2e2.png">

### 🎨 With the Color Scheme
*Click for full size.*

Choice of the Dragon | Choice of the Dragon | Multireplace Example
-------------------- | -------------------- | --------------------
<img alt="Custom1" src="https://user-images.githubusercontent.com/33694865/120052568-8f759680-bfeb-11eb-92dd-7f8d26eb50ad.png">|<img alt="Custom2" src="https://user-images.githubusercontent.com/33694865/120052891-2b53d200-bfed-11eb-9e47-c63be428005c.png">|<img alt="Custom3" src="https://user-images.githubusercontent.com/33694865/120053102-0875ed80-bfee-11eb-8962-d422ceb2769d.png">

If you want to use the ChoiceScript color scheme *only* with ChoiceScript files, you can do so by following these steps:

1. ddd

## Autocomplete Commands
The syntax includes some autocomplete commands written in an attempt to help writers quickly write common lines of ChocieScript code.

## Editing and Customization
This is a brief guide on how to edit and customize the syntax, its settings, and/or the color scheme, as well as how to create your own color scheme.

##### ⚠️ You are free to edit/customize/modify/etc this syntax definition and color scheme as much as you like for public or private use, so long as you link back here and do not in any way derive profit from it.

## Disclaimer
This syntax highlighter is in no way affiliated with or endorsed by Choice of Games, LLC. It is indepedently created and maintained by Fawkes (E.S. Fawkes) as an aid for writers.

ChoiceScript is &copy; D. Fabulich.
