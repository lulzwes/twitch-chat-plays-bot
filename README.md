# Twitch Chat Plays Bot
![GitHub Repo stars](https://img.shields.io/github/stars/lulzwes/twitch-chat-plays-bot?style=social)

A Python script for Twitch Chat interaction with almost any game.

----
### Prerequisites:
- Python https://www.python.org/downloads/ (tested with 3.10)
- Download Autohotkey from https://www.autohotkey.com/ and provide the .exe path to line 5 of the script. 
- Install ahk through pip - https://pypi.org/project/ahk/
- Get your Twitch oauth key from https://twitchapps.com/tmi/ (DO NOT SHARE THIS!), and paste the key on line 10 between the parentheses. 

----
### The Setup:

#### Line 5 - Replace 'PATH' with AHK .exe path location.
###### Example: 'C:\Program Files\AutoHotkey\AutoHotKey.exe'
    ahk = AHK(executable_path='PATH')

#### Line 10 - Add the oauth code that was generated from https://twitchapps.com/tmi/ here (include "oauth:" that is apart of the generated code).
###### DO NOT SHARE THIS KEY!
    PASS = "OAUTH_CODE"

#### Line 11 - Name the bot
    BOT = "BOT_NAME"

#### Line 12 - Add the name of the Twitch channel you want to monitor.
    CHANNEL = "CHANNEL_NAME"

#### Line 13 - Add your Twitch account name.
    OWNER = "ACCOUNT_NAME"

----
### Tweaking:

#### Game controls are handled by condition checks(if chat sends "up", AHK will read "up" and pass the command to the game). See below example, add and alter as you seem fit for each game.
###### You may need to go into game settings to reconfigure keymap for each game.

        if "up" == message.lower():
            ahk.key_press('up')
            message = ""

----
### Run the Script:
#### Navigate to the project directory using CMD or Terminal and run the command:
    py twitchchatplays.py
