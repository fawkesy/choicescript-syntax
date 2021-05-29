# ChoiceScript Syntax for Sublime

❕ **Version 1.0.0**

This is a custom syntax highlighter with custom autocompletes and optional color scheme created for [ChoiceScript](https://www.choiceofgames.com/about-us/). Developed to make reading and writing ChoiceScript code quicker and easier, with the included "ChoiceScript" color scheme it targets specific aspects of code to differentiate via color.

It is compatible with **Sublime 3** and **4**.

#### ⚠️ This is NOT an IDE like CSIDE.
It does not include a copy of ChoiceScript. It cannot run QuickTest or RandomTest. It does not check for bugs or errors. It does not include a word count. You **must** have a copy of [ChoiceScript](https://github.com/dfabulich/choicescript) (or [CSIDE](https://github.com/ChoicescriptIDE/main/releases)) on your computer or use the [web version of CSIDE](https://choicescriptide.github.io/web/) to run your game.

## 📖 Table of Contents
- [Features](#gem-features)
- [Installation](#hammer_and_wrench-installation)
- [Color Scheme](#art-color-scheme)
- [Screenshots](#camera_flash-screenshots)
- [Autocomplete Commands](#zap-autocomplete-commands)
- [Editing and Customization](#memo-editing-and-customization)
- [Disclaimer](#exclamation-disclaimer)

## :gem: Features
- Custom syntax highlighting for the ChoiceScript language.
- Full support for multireplace and stat charts.
- Custom color scheme for enhanced syntax highlighting.
- Autocomplete commands to quickly create common lines of code (page breaks, line breaks, choices, if/else statements, stat charts, comments, etc).
- Spell check for plain text and text for choice options and text in multireplace.
- Word wrap automatically enabled, tabs to indent conversion (for CSIDE compatiblity) enabled, auto match disabled (to keep from matching quotes).

## :hammer_and_wrench: Installation
The ChoiceScript syntax can be installed one of two ways.

### 📦 Package Control (recommended)
1. ddd

### 🛠 Manual Installation
1. ddd

## :art: Color Scheme
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

### ⚙️ Using the Color Scheme JUST for ChoiceScript
If you want to use the ChoiceScript color scheme *only* with ChoiceScript files, you can do so by following these steps:

1. With your ChoiceScript file active on Sublime, go to (MAC) Sublime Text > Preferences > Settings - Syntax Specific **OR** (PC) Preferences > Settings - Syntax Specific
2. A new window will open. On the left is the full range of Sublime settings you can configure. On the right is the settings configuration for that specific syntax.
3. In the file on the right, edit the file to look like this:

```
{
	"color_scheme": "ChoiceScript.sublime-color-scheme",
}
```
4. Save.

From now on, all files with ChoiceScript syntax will use the ChoiceScript color scheme, regardless of what your theme or overall color scheme is in the rest of Sublime.

## :camera_flash: Screenshots
Below are screenshots of the syntax, with and without the color scheme, featuring scene files from Choice of Games' [Choice of the Dragon](https://www.choiceofgames.com/dragon/) and my own project.

### ✨ Without the Color Scheme
*Click for full size.*

Sublime's Mariana | [One Dark Gravity](https://packagecontrol.io/packages/Theme%20-%20Gravity)
----------------- | -----------------
<img alt="Mariana" src="https://user-images.githubusercontent.com/33694865/120052569-900e2d00-bfeb-11eb-92a5-dc4f8bb19fc1.png">|<img alt="One Dark Gravity" src="https://user-images.githubusercontent.com/33694865/120052570-90a6c380-bfeb-11eb-9266-7f58db04fd67.png">
<img alt="Mariana2" src="https://user-images.githubusercontent.com/33694865/120053103-09a71a80-bfee-11eb-8b89-9b5739e65af3.png">|<img alt="One Dark Gravity2" src="https://user-images.githubusercontent.com/33694865/120053104-0a3fb100-bfee-11eb-8565-c4dac24893af.png">

[Solarized Light](https://packagecontrol.io/packages/Solarized%20Color%20Scheme) | [Solarized Dark](https://packagecontrol.io/packages/Solarized%20Color%20Scheme)
--------------- | --------------
<img alt="Solarized Light" src="https://user-images.githubusercontent.com/33694865/120052820-d1530c80-bfec-11eb-864b-dfffa547d5c3.png">|<img alt="Solarized Dark" src="https://user-images.githubusercontent.com/33694865/120052823-d1eba300-bfec-11eb-9491-ae385cf6c554.png">
<img alt="Solarized Light2" src="https://user-images.githubusercontent.com/33694865/120053108-0b70de00-bfee-11eb-9da1-b84ff6e1a6be.png">|<img alt="Solarized Dark2" src="https://user-images.githubusercontent.com/33694865/120053106-0ad84780-bfee-11eb-99b8-fcc7edf2a2e2.png">

### :sparkles: With the Color Scheme
*Click for full size.*

Choice of the Dragon | Choice of the Dragon | Multireplace Example
-------------------- | -------------------- | --------------------
<img alt="Custom1" src="https://user-images.githubusercontent.com/33694865/120052568-8f759680-bfeb-11eb-92dd-7f8d26eb50ad.png">|<img alt="Custom2" src="https://user-images.githubusercontent.com/33694865/120052891-2b53d200-bfed-11eb-9e47-c63be428005c.png">|<img alt="Custom3" src="https://user-images.githubusercontent.com/33694865/120053102-0875ed80-bfee-11eb-8962-d422ceb2769d.png">

## :zap: Autocomplete Commands
The syntax includes some autocomplete commands written in an attempt to help writers quickly write common lines of ChocieScript code.

### ❔ How to Use
All the autocomplete commands start with `cs_` and must either be at the beginning of a new line or following a whitespace, such as a space or tab. Upon entering `cs_`, Sublime will list all the available autocomplete commands. For the most part, you will only need to type in one or two characters after `cs_` for the right autocomplete. Sublime will commit to the autocomplete upon pressing `enter` or `tab`.

### 📋 List of Commands

Function | Trigger | Completion
-------- | ------- | -----------
Choice | `cs_ch` | <img width="448" alt="cs_ch" src="https://user-images.githubusercontent.com/33694865/120075916-d48bde00-c068-11eb-91fa-0e6235d38b67.png">
Page Break | `cs_pb` | <img width="448" alt="cs_pb" src="https://user-images.githubusercontent.com/33694865/120075561-6a266e00-c067-11eb-8c8d-72d2879f07a8.png">
Line Break | `cs_lb` | <img width="448" alt="cs_lb" src="https://user-images.githubusercontent.com/33694865/120075562-6a266e00-c067-11eb-8805-c40deb7f348d.png">
Multireplace | `cs_mr` | <img width="448" alt="cs_mr" src="https://user-images.githubusercontent.com/33694865/120075559-6a266e00-c067-11eb-9de8-de4cccaa2079.png">
If/Else | `cs_if` | <img width="448" alt="cs_if" src="https://user-images.githubusercontent.com/33694865/120075917-d5247480-c068-11eb-89e5-73e42492887d.png">
Comment | `cs_om` | <img width="448" alt="cs_om" src="https://user-images.githubusercontent.com/33694865/120075558-698dd780-c067-11eb-987a-cf89198609b4.png">
Stat Chart | `cs_st` | <img width="448" alt="cs_st" src="https://user-images.githubusercontent.com/33694865/120075721-0d778300-c068-11eb-87b7-45d509341429.png">
Horizontal Rule | `cs_hr` | <img width="448" alt="cs_hr" src="https://user-images.githubusercontent.com/33694865/120075557-698dd780-c067-11eb-939d-d43b0f8c7faf.png">
Implicit Control Flow | `cs_imp` | <img width="448" alt="cs_imp" src="https://user-images.githubusercontent.com/33694865/120075560-6a266e00-c067-11eb-96b3-6dde1e2ea378.png">
Startup.txt Header | `cs_header` | <img width="448" alt="cs_header" src="https://user-images.githubusercontent.com/33694865/120075565-6abf0480-c067-11eb-933e-b5f5c489b70b.png">

If need or desire ever arises, more autocomplete commands may be added in the future.

## :memo: Editing and Customization
This is a quick overview on how to edit and customize the syntax, its settings, and/or the color scheme, as well as how to create your own color scheme.

### Color Scheme
#### Sublime 4
1. (MAC) Sublime Text > Preferences > Customize Color Scheme. (PC) Preferences > Customize Color Scheme.
2. This will open a new window. On the left is the ChoiceScript color scheme I made, and on the right is a blank `.sublime-color-scheme` file.
3. Using the [Sublime Documentation](https://www.sublimetext.com/docs/color_schemes.html) and my color scheme code as a guide, customize the color scheme as you like. I have tried to be as thorough in my comments as possible to explain what affects which parts of the syntax.
4. Save it to your `/Packages/User` folder of your Sublime directory. Whatever changes you made will override my ChoiceScript color scheme.

Creating an entirely new color scheme follows a similar process. Ensure that your color scheme code includes a name --- `"name": "Your Color Scheme"` --- above `"variables"`.

#### Sublime 3
Editing a color scheme in Sublime 3 is not nearly as straight-forward as it is in Sublime 4. I recommend updating, but if you'd prefer not to, follow the instructions below.

1. Ensure that you have downloaded the files as instructed by the [Manual Installation](#hammer_and_wrench-manual-installation) section.


##### ⚠️ You are free to edit/customize/modify/etc this syntax definition and color scheme as much as you like for public or private use, so long as you link back here and do not in any way derive profit from it.

## :exclamation: Disclaimer
This syntax highlighter is in no way affiliated with or endorsed by Choice of Games, LLC. It is indepedently created and maintained by Fawkes (E.S. Fawkes) as an aid for writers.

ChoiceScript is &copy; D. Fabulich.
