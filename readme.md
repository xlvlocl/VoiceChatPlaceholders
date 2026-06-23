# Voice Chat Placeholders
Provides server-wide placeholders for servers using [Simple Voice Chat](https://modrinth.com/plugin/simple-voice-chat/).

These placeholders can be used in nametag plugins such as [UnlimitedNameTags](https://www.spigotmc.org/resources/unlimitednametags.117526/) 
which replaces the default nametags, or in any other plugin that supports PlaceholderAPI.

This plugin does **not** render icons by itself, it only exposes placeholders.

## Features
- Exposes `%vcicon_status%` placeholder
- For custom icons, create them in your server resource pack and use them in the `config.yml`
- To reload config use `/vcp reload` with op permissons
- Supported states:
  - talking
  - whispering
  - quiet
  - disabled
  - not_installed

## Requirements
- Paper 1.21
- Server Resource Pack that includes the configured icons
- [Simple Voice Chat](https://modrinth.com/plugin/simple-voice-chat/)
- [PlaceholderAPI](https://www.spigotmc.org/resources/placeholderapi.6245/)

## Placeholders
| Placeholder | Description                                     |
|-------------|-------------------------------------------------|
| `%vcicon_status%`  | Is replaced with the configured voice chat text |

## Configs

### config.yml
```yaml
talking: "🔊"
whispering: "🔉"
quiet: "🔊"
disabled: "🔇" # when the player is connected but e.g. muted
not_installed: "❌" # when the player does not have the the mod installed
talk_timeout_ms: 300 # Time in milliseconds after which the talking icon stops. 300 works well for most use cases.

NOTE: You can set "🔊" to talking, whispering, quiet
to show only that player can talk and 🔇 to not_installed and
disabled for binary icon. Or even use javascript in PlaysholderAPI to
manage icons and make more playsholders yourself
```
