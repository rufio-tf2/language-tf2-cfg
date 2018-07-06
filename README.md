# TF2 cfg syntax highlighting

Adds syntax highlighting support for `.cfg` files

## Features

<table>
  <tr>
    <td><img src="./images/b4nny_no_highlighting.png" alt="Example without syntax highlighting" /></td>
    <td><img src="./images/b4nny_with_highlighting.png" alt="Example with syntax highlighting" /></td>
  </tr>
</table>

<blockquote>
  <p>Taken from b4nny's <a href="https://drive.google.com/file/d/1S9bcuSHauGUSNlrOP93zm5kOlynnWG8V/view" target="_blank">config</a></p>
</blockquote>

This is the grammar I'm looking for:

- Comment
- Command
  - Unknown (deprecated, unused, or just unknown)
  - Buttons (`SPACE`, `MOUSE1`)
  - Actions (`+attack`, `say_team`)
  - Settings (`bind`, `r_drawviewmodel`)
- Numberic-Literal
- Variable (custom commands)
- Command List (`"+jump; +duck; +attack;"`)
- Punctuation-Semicolon

## Known Issues

- Not [all](https://developer.valvesoftware.com/wiki/List_of_TF2_console_commands_and_variables) commands have been included yet
- Lazy regex checking, such as `r_\\w+` to mark anything that starts with `r_`, but really should only include exact commands
- My regex has not been reviewed and there's potentially a smarter way to be doing some of the things
- JavaScript name scopes should probably be replaced with something more generic (e.g. `variable.other.readwrite.js`)

## Release Notes

Users appreciate release notes as you update your extension.

### 0.0.1

:construction: Still getting things into shape.
