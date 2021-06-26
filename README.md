# ChoiceScript Syntax for Sublime

❕ **Version 1.0.0**

This is a custom syntax highlighter with custom autocompletes and optional color scheme created for [ChoiceScript](https://www.choiceofgames.com/about-us/). Developed to make reading and writing ChoiceScript code quicker and easier, with the included "ChoiceScript" color scheme it targets specific aspects of code to differentiate via color.

It is compatible with **Sublime 3** and **4**.

#### ⚠️ This is NOT an IDE like CSIDE.
It does not include a copy of ChoiceScript. It cannot run QuickTest or RandomTest. It does not check for bugs or errors. It does not include a word count. You **must** have a copy of [ChoiceScript](https://github.com/dfabulich/choicescript) (or [CSIDE](https://github.com/ChoicescriptIDE/main/releases)) on your computer or use the [web version of CSIDE](https://choicescriptide.github.io/web/) to run your game.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Color Scheme](#color-scheme)
- [Screenshots](#screenshots)
- [Autocomplete Commands](#autocomplete-commands)
- [ChoiceScript Tips](#choicescript-tips)
- [Editing and Customization](#editing-and-customization)
- [Contact Me](#contact-me)
- [Disclaimer](#disclaimer)

## Features
- Custom syntax highlighting for the ChoiceScript language.
- Full support for multireplace and stat charts.
- Custom color scheme for enhanced syntax highlighting.
- Autocomplete commands to quickly create common lines of code (page breaks, line breaks, choices, if/else statements, stat charts, comments, etc).
- Auto-indent following appropriate lines of code (`*choice`, `#options`, `*if/else`, `*stat_chart`).
- Spell check for plain text and text for choice options and text in multireplace.
- Word wrap automatically enabled, tabs to indent conversion enabled, auto match disabled (to keep from matching quotes).

## Installation
The ChoiceScript syntax can be installed one of two ways, regardless of whether you're using Sublime 3 or 4:

### 📦 Package Control
1. In Sublime, go to Tools > Install Package Control...
2. Open the Command Palette by pressing (MAC) CMD + Shift + P **OR** (PC) CTRL + Shift + P.
3. Type `Package Control: Install Package` into the Command Palette.
4. In the new Package Control window, type `ChoiceScript` with no spaces.
5. Select "ChoiceScript" to install the syntax and color scheme.
6. On a `.txt` scene file, go to the bottom right of the Sublime window where it says "Plain Text." Click it and select "ChoiceScript" from the list of syntaxes.
7. You're now ready to write ChoiceScript in Sublime!

### 🛠 Manual Installation
1. On this repository, click "Code" above the files.
2. Select "Download ZIP" and if prompted, choose where to save the folder.
3. Extract the contents of the zipped folder.
4. In Sublime, go to (MAC) Sublime Text > Preferences > Browse Packages... **OR** (PC) Preferences > Browse Packages... to open your Sublime `Packages` folder.
5. Copy and paste the extracted `ChoiceScript` files directly into the `Packages` folder.
6. In Sublime, on a `.txt` scene file, go to the bottom right of the Sublime window where it says "Plain Text." Click it and select "ChoiceScript" from the list of syntaxes.
7. You're now ready to write ChoiceScript in Sublime!

#### 🌈 Using the Color Scheme
1. Go to (MAC) Sublime Text > Preferences > Select Color Scheme **OR** (PC) Preferences > Select Color Scheme. (On Sublime 3, it's "Color Scheme...")
2. Select the "ChoiceScript" color scheme.
3. You're now all set with the ChoiceScript syntax highlighter and custom color scheme!

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

## Screenshots
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

### ✨ With the Color Scheme
*Click for full size.*

Choice of the Dragon | Choice of the Dragon | Multireplace Example
-------------------- | -------------------- | --------------------
<img alt="Custom1" src="https://user-images.githubusercontent.com/33694865/120052568-8f759680-bfeb-11eb-92dd-7f8d26eb50ad.png">|<img alt="Custom2" src="https://user-images.githubusercontent.com/33694865/120052891-2b53d200-bfed-11eb-9e47-c63be428005c.png">|<img alt="Custom3" src="https://user-images.githubusercontent.com/33694865/120053102-0875ed80-bfee-11eb-8962-d422ceb2769d.png">

## Autocomplete Commands
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

## ChoiceScript Tips
These are some general quality of life tips for writing ChoiceScript, especially in Sublime.

- **Use Dropbox for your files!** Dropbox is free and easy to access across every device and operating system. Keeping your ChoiceScript scene files in a Dropbox folder ensures that you will *never* lose your files, and because of its version history feature, it's easy to go back to an older version of your file if you've made a mistake.

- **Get a word count plugin for Sublime.** This is easily done through Package Control. Simple open Command Palette, type in "WordCount" and install the [top result](https://packagecontrol.io/packages/WordCount). This will add a word count to the bottom left corner of the Sublime window. The plugin counts *all* words, including command lines, and you cannot quickly find out the total word count for a project without manually adding the word counts together.

- **Take advantage of columns and split view in Sublime.** Sublime lets your open multiple columns (View > Layout), so you can view two files at once. These can be two separate files or the same file (split view). To use split view, go to File > Split View. You may need to adjust the layout, but it's very easy to do.

- **Use keybindings for em dashes and ellipsis.** If you'd prefer your writing to use proper em dashes, "—", or ellipsis, "…", it is very easy to set Sublime up to automatically convert "--" and "..." for you using keybindings. Go to (MAC) Sublime Text > Preferences > Key Bindings **OR** (PC) Preferences > Key Bindings. A new window will pop up with two files. Copy and paste the following into the file on the right between the `[]` brackets and save:
```
	{ "keys": ["-", "-"], "command": "insert_snippet", "args": {"contents": "—"} },
	{ "keys": [".", ".", "."], "command": "insert_snippet", "args": {"contents": "…"} },
```
- **Use CSIDE.** Opting to use [CSIDE](https://github.com/ChoicescriptIDE/main/releases) instead of downloading the [ChoiceScript folder](https://github.com/dfabulich/choicescript) from Github can make working with ChoiceScript easier. CSIDE has basic ChoiceScript syntax highlighting, a copy of ChoiceScript and its tests built into it, and has a good word count feature that excludes command lines and will look at the word count for your overall project -- and it has a browser version, so you don't need to download anything. It *also* has a console, which you can read about in its documentation.

- **Use CSIDE and Sublime together.** Writing code in Sublime and then using CSIDE to test and make immediate bug fixes is a solid way to develop ChoiceScript games. You get the benefits of Sublime -- a more precise syntax highlighter and autocomplete commands -- and the advantages of CSIDE, such as its console. Sublime will update with any saved changes you make in CSIDE. CSIDE does not update on its own, but it is very easy to reload scene files, either by right clicking on the file you wish to reload in the left sidebar or going to Project > Reload All Files.<br><br>In the event you make a mistake while saving in either program and accidentally lose anything, if you're storing your files on Dropbox, it's very easy to recover lost content using version history.

## Editing and Customization
##### ⚠️ This syntax definition and color scheme are provided under the [MIT license](https://tldrlegal.com/license/mit-license).

This is a quick overview on how to edit and customize the syntax definition, its settings, and/or the color scheme, as well as how to create your own color scheme.

### 🎨 Color Scheme
#### 🔹 Sublime 4
1. (MAC) Sublime Text > Preferences > Customize Color Scheme. (PC) Preferences > Customize Color Scheme.
2. This will open a new window. On the left is the ChoiceScript color scheme I made, and on the right is a blank `.sublime-color-scheme` file.
3. Using the [Sublime Documentation](https://www.sublimetext.com/docs/color_schemes.html) and my color scheme code as a guide, customize the color scheme as you like. I have tried to be as clear and thorough as possible with my comments to explain what affects which parts of the syntax.
4. Save it to your `/Packages/User` folder of your Sublime directory. Whatever changes you made will override my ChoiceScript color scheme.

Creating an entirely new color scheme follows a similar process. Ensure that your color scheme code includes a name -- `"name": "Your Color Scheme"` -- above `"variables": {}`.

#### 🔸 Sublime 3
Editing a color scheme in Sublime 3 is not nearly as straight-forward as it is in Sublime 4. I recommend updating, but if you'd prefer not to, follow the instructions below.

1. Ensure that you have at least downloaded the `ChoiceScript.sublime-color-scheme` file via the [Manual Installation](#-manual-installation) option.
2. In Sublime, open `ChoiceScript.sublime-color-scheme`. You can edit this file directly to make changes to the color scheme.
3. Using the [Sublime Documentation](https://www.sublimetext.com/docs/color_schemes.html) and my color scheme code as a guide, customize the color scheme as you like. I have tried to be as clear and thorough as possible with my comments to explain what affects which parts of the syntax.
4. Save, either as a new file with the `.sublime-color-scheme` extension in the `/Packages/User` folder of your Sublime directly or simply save it as `ChoiceScript.sublime-color-scheme` to completely overwrite my color scheme.

Creating an entirely new color scheme is an almost indentical process. Simply save it as an entirely new file with a different name and ensure that the code includes a name -- `"name": "Your Color Scheme"` -- above `"variables": {}`.

### ⚙️ Syntax-Specific Settings
Modifying syntax-specific settings in Sublime is very easy.

1. (MAC) Sublime Text > Preferences > Settings - Syntax Specific. (PC) Preferences > Settings - Syntax Specific.
2. A new window will open will two files. One the left is a read-only file that list all possible settings you can modify and their default value in Sublime. On the right is a new syntax-specific settings file that will override all other settings, including the ones I have set for `ChoiceScript.sublime-settings`.
3. Using the file on the left as a guide, write your new settings for the ChoiceScript syntax.
4. Save.

Alternatively, if you have downloaded the `ChoiceScript.sublime-settings` files via [Manual Installation](#-manual-installation), you can edit the settings I've set directly. I have included comments in the files for that purpose.

Below are the settings I've set for the ChoiceScript syntax:
```
{
		// remove or comment out to disable
		// if you want to use your default scheme
		// or one of the other choicescript schemes
	//"color_scheme": "Packages/User/ChoiceScript.sublime-color-scheme",

		// change to false to disable entirely
	"auto_complete": true,

		// scope for cs_ command autocompletes
	"auto_complete_selector": "keyword.trigger",

		// change to false to disable entirely
	"spell_check": true,

		// so it only spell checks plain text and
		// text in multireplace and choice options
	"spelling_selector": "string.text, -(comment, entity, keyword, variable, storage)",

		// general quality of life and compatibility
		// stuff so your code works in other editors
	"word_wrap": true,
	"tab_size": 2,
	"detect_indentation": true,
	"auto_indent": true,
	"smart_indent": true,
	"use_tab_stops": true,
	"translate_tabs_to_spaces": true,
	"margin": 7,

		// makes the caret blink
	"caret_style": "blink",

		// lets you scroll past the last line in a
		// file to making writing final lines more
		// comfortable
	"scroll_past_end": true,

		// disabled so it doesn't match quotes
	"auto_match_enabled": false,
}
```
### 📝 Syntax Definition
Like all syntax definitions in Sublime 3 and beyond, the ChoiceScript syntax definition uses YAML, which is remarkably straight forward and intuitive, and RegEx (regular expression) which is less so. I'm not going in-depth on how to write in regular expression or how to write a new syntax definition, but I'll briefly go over how you can edit my syntax definition or create your own and link to some resources.

1. Ensure that you have at least downloaded the `ChoiceScript.sublime-syntax` file via the [Manual Installation](#-manual-installation) option.
2. In Sublime, open `ChoiceScript.sublime-syntax`. You can edit this file directly to modify the syntax definition.
3. Using the [Sublime Documentation](http://www.sublimetext.com/docs/syntax.html) and [Oniguruma Regular Expressions](https://raw.githubusercontent.com/kkos/oniguruma/5.9.6/doc/RE), modify the syntax definition as you please.

**Note:** This is my first syntax definition. I have probably done a lot wrong, I'm sure, so I don't recommend using my syntax definition as a guide on how syntax definitions are supposed to look/work.

4. Save, either as a new file with the `.sublime-color-scheme` extension in the `/Packages/User` folder of your Sublime directory or simply save it as `ChoiceScript.sublime-syntax` to completely overwrite my syntax definition.

Creating an entirely new syntax definition is very easy. Go to Tools > Developer > New Syntax... and Sublime will open a new file set up for a syntax definition.

I found the Oniguruma Regular Expression Document difficult to understand as I had no prior knowledge of regular expression. I found [this cheatsheet](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions/Cheatsheet) helpful, though it is meant for *JavaScript* and not necessarily Sublime syntax definitions. Referencing both is the best route, but at the end of the day, the best way to figure it out is trial and error.

## Contact Me
If you need to contact me directly for any reason relating to the ChoiceScript syntax, you can do so.

**Discord:** Fawkes#4253<br>
**COG Forum:** [Fawkes](https://forum.choiceofgames.com/u/fawkes/)<br>
**Tumblr:** [@fantasyfawkes](https://www.fantasyfawkes.com/)

## Disclaimer
This syntax highlighter is in no way affiliated with or endorsed by Choice of Games, LLC. It is indepedently created and maintained by Fawkes (E.S. Fawkes) as an aid for writers.

ChoiceScript is &copy; D. Fabulich.
