# Latex Snippets for Visual Studio Code

Common snippets to write faster LaTeX

## Installing

* Install the [HyperSnips](https://github.com/draivin/hsnips) extension.
* Open the HyperSnips directory (Ctrl + Shift + P, "HyperSnips: Open Snippets Directory") and copy there the file `hsnips/latex.hsnips`
* From the hsnips folder in previous entry, up one folder and down again into `snippets`. Copy there the content of `vscode/latex.json`
* Set keybindings with Ctrl + Shift + P, and "Preferences: Open Keyboard Shortcuts (JSON)". Copy there the content of `vscode/keybindings.json`
* You may also install the `LaTeX Workshop` extension, but some snippets may conflict. You can disable the snippets from that extension thanks to another extension: `Control Snippets`.

### Usage

Simply open a `.tex` file and start typing. All "static" snippets are contained in `latex.json`, and are expanded by typing their "prefix" and pressing `Tab` (or `Enter`, if they appear in the IntelliSense menu). You can navigate between fixed placeholders with `Alt + LeftArrow` and `Alt + RightArrow`.

There are also "dynamic" snippets, that automatically expands after typing a certain trigger. For example:
* `mk` expands in `$ $ `. Note that the final space is automatically removed if you type certain characters (e.g. `-?:,`) after the last `$`.
* An alphabetical character repeated two times is automatically converted to the corresponding greek letter: e.g. `aa` becomes `\alpha`. This does not conflict with words with repeated letters (e.g. `letters`) or with other commands (e.g. `\ddot`).
* Type `M3x3` and a space to obtain a 0-filled 3x3 matrix. Dimensions can be changed dynamically: `M2x6` works too. If you type a `d` instead of the final space, the resulting matrix will have navigable placeholders only on the diagonal.
* Type `dfdx` and a space to write a partial derivative. Use a capital `D` at the start if you want the usual derivative.
* Vectors can be set by typing a character (or word) followed by `.,` or `,.` (just press the two keys at the same time, as their order does not matter). Similar commands automatically convert strings like `p-hat`, `pbar`, `Pcal` (to `\mathcal{P}`). For `\mathbb{P}` use `P#`. 
* Many more! Look at `latex.hsnips` for all the implementations.

### Latex extension snippits

https://github.com/James-Yu/LaTeX-Workshop/issues/1974

Actually, there is a way to hide the snippet you don't like. I for example disliked, that whenever I type "." a suggestion for "\dots" pops up and when I hit enter (on the end of a phrase) this snippet is inserted. To avoid this, use CTRL+ALT+P, search for "Insert Snippet", hit enter, seach for the snippet you don't want to be shown and hit the eye-icon at the right to hide it for intellisense.  

https://code.visualstudio.com/docs/editor/userdefinedsnippets#_can-i-remove-snippets-from-intellisense    
Yes, you can hide specific snippets from showing in IntelliSense (completion list) by selecting the Hide from IntelliSense button to the right of snippet items in the Insert Snippet command dropdown.
You can still select the snippet with the Insert Snippet command but the hidden snippet won't be displayed in IntelliSense.
