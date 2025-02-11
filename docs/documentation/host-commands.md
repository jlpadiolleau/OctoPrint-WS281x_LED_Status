---
description: The plugin reacts to a number of @ commands, this will tell you the details.
---

# Host @ Commands

From [OctoPrint's documentation](https://docs.octoprint.org/en/master/features/atcommands.html):

> @ commands (also known as host commands elsewhere) are special commands you may include in GCODE files streamed through OctoPrint to your printer or send as part of GCODE scripts, through the Terminal Tab, the API or plugins. Contrary to other commands they will never be sent to the printer but instead trigger functions inside OctoPrint.

The plugin reacts to some different @ commands, listed below:

| Command             | Explanation                                         |
| ------------------- | --------------------------------------------------- |
| `@WS LIGHTS_ON`     | Turns lights on, same as pressing switch in navbar. |
| `@WS LIGHTS_OFF`    | Turns lights off.                                   |
| `@WS LIGHTS_TOGGLE` | Toggles lights on/off.                              |
| `@WS TORCH`         | Activates the torch mode, for timer mode            |
| `@WS TORCH_ON`      | Turn torch on, for toggle mode                      |
| `@WS TORCH_OFF`     | Turn torch off, for toggle mode                     |

These commands can be used in g-code scripts, or in custom controls in apps - see here for [instructions for OctoRemote](https://github.com/cp2004/OctoPrint-WS281x\_LED\_Status/issues/6#issuecomment-668110507), or the guide on how to create a [timelapse flash in OctoLapse](../guides/octolapse-flash.md) which also uses @ commands.

{% hint style="info" %}
**Seeing a warning about a deprecated @ command being used?**

In version 0.8.0 of the plugin, the format of the commands changed. The old style commands still work, but you should switch to using the new style, as documented above. Support for the deprecated @ commands will be removed in a future version.
{% endhint %}
