# Annoying Nico-style Twitch-Chat Overlay
Scrolls twitch chat across your entire monitor like nicovideo comments, always on top, and has a couple other stupid easter eggs too.

# Visual demos if you don't feel like reading

General explantion
https://youtube.com/shorts/ZhQ4CmZlnFg

Showing off the emote spam, with phone cam to explain how blinding it can be (older, worse version)
https://www.tiktok.com/@namaztak/video/7595529247767170359

# Usage
Run the executable, let it authorize on your Twitch account on its first run. Every subsequent run will still open your browser to give the overlay its authorization token.  
The overlay doesn't connect to anything but Twitch, and doesn't even store anything locally. The only time anything about the program will change is if I make a new version and you come back here to download it yourself.
As soon as you see "Redirect token to Godot" you can close the browser window.  
You now have an invisible Godot window spanning the entire monitor ***where your mouse was when you launched it.*** If it launched on the wrong monitor, kill it and launch it again from the monitor where you play your games.  
It pulls every chat message as it comes in, picks a random font and size for each message, and scrolls that message across your entire monitor.  
***Just capture it in OBS using Game Capture, and be sure to check the "Allow transparency" box.*** Then fit it to your canvas (if not using a 16:9 monitor, recommend placing it centered horizontally, in relation to your gameplay or whatever else you put on your stream.)

If you want your chat to be able to troll you slightly harder, they can type "!purple" into your chat, and it'll turn your entire monitor purple for 30 seconds (3 minute cooldown).

Every font you have installed (minus a small handful of illegible ones I've identified and filtered out from random selection) goes into the pool for fonts that can be chosen per-message.  
More fonts, more variance.

Messages can range in size from 1/40th of your monitor height, to 1/5 under normal circumstances.  
Subscriptions/gift subs will scroll an ENORMOUS wavy rainbow message with a randomly chosen string appended to it. Sub triggers' messages are hard-coded to be half your monitor's height, and guaranteed to be dead center vertically. A sound effect will also play.  
Slightly less enormous wavy rainbow messages will appear when anyone follows your channel. A sound will also play for follows.

You, the streamer only, can also use !adbreak to make it automatically run 3 minutes of ads and set a 55-ish minute timer that will play a sound effect and post "3-minute ad break soon." in your chat, to remind you to rerun them hourly to prevent pre-rolls. You don't have to use this if you don't feel like it, or would wanna manage your ad schedule some other way. (!adbreak will always trigger this, though, so sorry if that conflicts with something else you've set up.)

# Some minor caveats/intentional jank
* You can't focus the window to click on it, so you either have to kill it from the task manager, or keep it pinned to your taskbar and kill it from there.  
* Run all your games in some windowed form (actual windowed or borderless), or it's really not gonna work. It needs to be able to be on top of your games/other programs.  
* If you use the Linux build, it doesn't work properly on Wayland, because apparently Wayland doesn't let the mouse pass through things to what's behind them. X11 works fine, but if you see it offset vertically, make sure you have your taskbar set to allow things to go behind it.  
* Just because I'm lazy with wanting to play Whack-a-mole with lazy spambots, there's code to automatically ban anyone for including BOTH "ai" and "viewers" in their message. If that ever happens without you meaning to ban somebody that was discussing it, just tell the chatter not to say both of those things in one message.
* If you don't want the sound effects, cause you use something else and feel like it clashes, just don't capture the audio from the overlay in OBS, and mute it in Windows. (The program Eartrumpet is useful for this if you don't already use it.)
* Emotes do not appear in-line with their messages, and instead are all spawned individually with their own random Y-position and scale between 6 sizes, scrolling across at their own speeds. If anyone wants to teach me how to fix this, I will.  

# Stuff this thing relies on  
[Obviously Godot itself](https://godotengine.org/)  
[Twitcher](https://github.com/kanimaru/twitcher)  
[This Godot extension for mouse passthrough on Windows](https://github.com/hubacekjakub/Godot-WinMousePassthrough)  

# Donate?  
If you feel like it, pay me. You don't have to. Or if you want me to add a feature either for general use, or yourself specifically, lemme know what the idea is, and if I think I can do it, you can pay me to do it.  
https://ko-fi.com/nam_137
