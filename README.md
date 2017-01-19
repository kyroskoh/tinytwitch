# tinytwitch
tinytwitch is a twitch chat viewer with not many features (no emotes, you can only view chat, etc) but a very small footprint
([under 2mb ram and around 0.02 average cpu usage when connected to the current top 10 streamer's chats](http://i.imgur.com/frpVkMO.png))

This makes it much more lightweight than using a browser and much more simple than using a full IRC client just for twitch

If you're just looking for the downloads, [click here](https://github.com/smt923/tinytwitch/releases) 

The current supported features are:

* Allows joining multiple channels (can look messy)
* Optional "highlights" (as you don't login it might be worth highlighting your username)
* Optional logging to file in same directory
* Settings file to set up default settings as well as colors
* Shows users joining and leaving a chat
* Shows mod gain and loss messages (mostly when mods join)
* [S]ubscriber and [M]oderator badges
* New subs and resubs notifications with number of months, both with their message

![tinytwitch](http://i.imgur.com/t6B0Syj.png)

## Usage
Either run the program with the streamer's chatrooms as arguments:
```
tinytwitch.exe bobross summit1g lirik
```
Or run the program and it will prompt you to enter streamers in the same format:
```
$ tinytwitch.exe
Type the usernames of the channels to join, seperated by a space:
bobross summit1g lirik
``` 
You can of course just enter a single channel

## What is it for?
This was mostly made for fun and to test the awesome language it's made in, [Nim](http://nim-lang.org/). You'll probably immediately know if you have use for this or not, if you don't feel like
leaving a resource hog browser running but still want your chat up, or maybe you want to leave a friend's/streamer you moderate's
chat up while playing a game and lanuch a browser when you need to step in and moderate

## Building
You'll need [Nim](http://nim-lang.org/) to build the program your self, simply running
```
$ nimble install
``` 
should install the program, or it can be built simply with
```
$ nim c -d:release tinytwitch.nim
```
though you will need to install the [irc module](https://github.com/nim-lang/irc) if you don't use nimble to automatically get the dependency
