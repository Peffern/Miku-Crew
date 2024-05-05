# Miku-Crew
Put Hastune Miku onboard the Kestrel!

## Is she replacing someone?
She's taking the spot that rightfully belongs to her.

## Dependencies
This uses Slipstream Mod Manager.
This should go after any other mods that change crew names. It should be compatible with any of the existing languages, and should behave nicely with any added languages or name lists.
If mods use multiple nameLists per language, Miku will show up multiple times. (The base game also does this, but there's a workaround in that specific case).

### How it works
After making a spot for Miku, she is added to every `<nameList sex="female">` entry in `names.xml`. In the base game of FTL, the English (default) name list is in two pieces, for some reason, so Miku as added twice. To work around this, the mod marks every list containing "Kara", then unmarks every list containing "Lexie". This leaves the mark only on the second English list, while leaving any additional lists unmarked. Then, Miku is removed from the marked list, along with the mark. This means she only shows up on one English list, while keeping her on every other language's list. This is necessary because Slipstream can't search for a negative.

Her name is localized into every non-Latin language in the base game (simplified Chinese, Japanese, and Russian), and is in Latin characters in every other context.
Other mods' nameLists will be processed in the above manner, which should cover most cases.

## Installation
Download `miku.ftl` from this repository and put it in Slipstream's `/mods` folder.
