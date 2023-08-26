# TF2 cfg syntax highlighting

Adds syntax highlighting support for `.cfg` files

## Features

<blockquote>
  <p> Example config</a>
</blockquote>
<table>
  <tr>
    <td><img src="https://i.imgur.com/XmgBBVj.png" alt="Example without syntax highlighting" /></td>
    <td><img src="https://i.imgur.com/Y43gI9s.png" alt="Example with syntax highlighting" /></td>
  </tr>
  <tr>
    <td><i>Plain Text</i></td>
    <td><i>Using the <code><b>Monokai Pro</b></code> theme</i></td>
  </tr>
</table>

### Used grammar

- ### string.quoted.double.cfg
  Used in say, echo & exec.
- ### variable.other.readwrite.cfg
  Normal text, alias commands, unrecognized commands.
- ### constant
  - ### .numeric
    ConVar constants, numbers.
  - ### .other.key
    `MOUSE1`, `SPACE`, `F3`
- ### comment.line.double-slash.c
  Comments
- ### support
  - ### .function
    - ### .cfg.toggle
      Action commands: `+attack2`, `-jump`, `+use_action_slot_item`.
    - ### .cfg.argument
      Argument action commands: `wait 3`, `taunt_by_name Taunt: Schaudenfreunde`, `addcond 91`.
    - ### .cfg.trigger
      Trigger action commands: `kill`, `mp_forcewin`, `voice_menu1`.
  - ### .variable
    - ### .cfg
      Console commands: `mat_picmip`, `sv_cheats`, `sensitivity`.
    - ### .cfg.addon
      Addon commands: `prec_mode`.
- ### invalid.deprecated.cfg
  Deprecated commands and actions: `g_ragdoll_fadespeed`, `god`, `mat_parallaxmap`.

## Install

<ol>
  <li><a href="https://code.visualstudio.com/Download">Download</a> VS Code</li>
  <li>
    <p>Install the extension</p>
    <img src="https://i.imgur.com/IeOIXzc.png" alt="Install through VS Code" height="50%" width="50%" />
  </li>
  <li>
    <p>Press reload</p>
    <img src="https://i.imgur.com/oN28TYy.png" alt="Reload VS Code" height="50%" width="50%" />
  </li>
</ol>

## Setup

<img src="https://i.imgur.com/ARqR6MK.png" height="75%" width="75%" />

1.  Open a `.cfg` file
1.  Click at the bottom right to change its "File Association" (Or press `Ctrl+K, Ctrl+M`)
1.  Select, `Configure File Association for '.cfg'...`
1.  Select `TF2 cfg` from the list

### Alternatively...

You can open your user settings (`Ctrl+,`) and add

```json
"files.associations": {
  "*.cfg": "TF2 cfg"
}
```

## Theme

Note that you can change/control the [Color Theme](https://code.visualstudio.com/docs/getstarted/themes):

<img src="https://i.imgur.com/7teYynx.png" height="75%" width="75%" />

## Known Issues

- My regex has not been reviewed and there's potentially a smarter way to be doing some of the things
- Ideally there'd be a custom color theme with property scope names (currently I'm using at least one `.js` name)

## Release Notes

### v0.0.8

- Improved regular expression.
  - Added matches for all Team Fortress 2 commands.
  - Improved syntax highlighting for strings and command chains.
  - Shortened regex.
- Improved syntax highlighting for themes.
### v0.0.7

- Renamed the settings rule to commands.
- Fixed bind and unbind key regular expression.
- Added regular expression for `set*` commands.
- Created a pattern for echo strings
- Fixed partial variable rule matches inside strings.
- Added several more matches for TF2, P-REC, and HLAE commands.

### v0.0.6

- Improved regular expression

## Unlicense

This is free is all senses of the word. [UNLICENSE](./UNLICENSE)
