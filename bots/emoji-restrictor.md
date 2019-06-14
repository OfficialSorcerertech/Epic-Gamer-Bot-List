## Overview

Did you know Discord had the ability to make a custom emoji only available to
certain roles? If you didn't, that is because they don't offer an easy way to
use that function. Enter, Emoji Restrictor!

* [Add to your Guild](https://discordapp.com/api/oauth2/authorize?client_id=553619116775309332&permissions=1074023425&redirect_uri=https%3A%2F%2Fdiscord.gg%2F9prGCXT&response_type=code&scope=bot)
* [Support Server](https://discord.gg/9prGCXT)

## Example
Here is what a user of your server may see on the Discord's Emoji
Picker:

![many emotes](https://serious.garantiertnicht.software/p/398d96e35e3c8ac54b3d56afc27c390573a77084)

With the power of Emote Restrictor, another user may see this:

![fewer emotes](https://serious.garantiertnicht.software/p/797099f2f74ed71d18c87cc436413066031e69a4)

Note that the other user has significantly less emotes? That's what this bot can
do.

## Usage
Commands include  `add` which allows a role to use the mentioned emojis
and `remove` which removes the role from the whitelist again with the added
bonus of `query` to get the roles allowed to use an emote.

**Admins and the owner are not except from the restrictions.** If you want to
keep using the emotes you are restricting, add at least one of your roles to the
list of allowed roles.

### Command Examples:
* `` @EmojiRestrictor#6662 add :awesome_emote: `Admins` ``
* `@EmojiRestrictor#6662 query :awesome_emote: `
* `` @EmojiRestrictor#6662 remove :awesome_emote: `Admins` ``

In-chat-help is available with `help` and `help <command>`

## Why we need the permissions we ask for
Trusting things can be hard, so here's what we use the permissions for:
* **Read Messages**: As this bot has commands, we must be able to read them. You
  can grant this permission on a channel-per-channel basis tho (if you only need
  it in a bot commands channel, for example)
* **Send Messages**: We also need to answer to these commands. The same thing as
  above applies.
* **Embed Links**: A huge blob of text doesn't look good. That's why we'd like
  to use nice embeds. The time it takes to write a separate function to deal
  with it not being allowed isn't worth it so this is required.
* **Manage Emoji**: We can't say Discord what roles you'd like to whitelist
  without this permission. Required for the `add` and `remove` commands.
* **Use External Emotes**: In the help command for add, remove and query we show
  examples. In order to have an emote ready even if you don't have any, we have
  one set up - on our server. We will only ever use this in help.
* **Create Instant Invite**: This is mainly here for support reasons. If you
  have a problem it makes it easier to check it out in person if needed. If you
  would not like any visits from me this can safely be revoked.

**Do not grant this bot any other permissions.** It isn't needed and will only
increase the attack surface if the bot ever gets compromised. Giving the bot
additional permissions anyways may result in the bot refusing to work.

## Open Source
This bot is Free Software licensed under AGPL 3 or later. You can view the source [here](https://gitlab.com/garantiertnicht/emoji-restrictor).

