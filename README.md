# moderator-scanner
Moderator Scanner. A Roblox plugin that scans your game for any ToS breaking content (other than images and audio sadly)

(From the Roblox Developer Forum since there's no point in writing this again)

Here's [my devforum post](https://devforum.roblox.com/t/moderator-scanner-that-plugin-thats-got-your-back/2802965) on Moderator Scanner if you don't like GitHub's text formatting; and also because it has more information and will be updated.

<br>
<br>

# Moderator Scanner - Version 1 (v1) by D00M3D_Dev
### It’s Got Your Back.


Get the plugin [here](https://create.roblox.com/store/asset/16021836300/Moderator-Scanner)

<br>
<br>

## Why Use Moderator Scanner?
##### Why should you use my plugin?


You should use my plugin if you’re suspicious of other developers working on your game that might try to pull a sneaky move by making some object have an inappropriate name or displaying a TextLabel to your players with something along the lines of promoting their social media.

Or you could use it to make sure you don’t accidentally screw up and do something that might risk an account moderation action.

<br>

## Moderator Scanner’s Cons
##### The cons with the plugin

<br>

You can find this on my Devforum post since this is subject to change

<br>

## Understanding The Way The Plugin Scans And How I Came Up With The Idea
##### You can skip this part and go to the “Using The Plugin” section if you don’t care about the way it scan stuff

<br>

I was thinking of what I should create as my first ever “real plugin” before I came up with the idea a few weeks later. And well, a few weeks later while in a topic about a game that was somehow still up, I came up with the idea to make a plugin that warns you about stuff in your game that could be bad. The idea did not directly stem from the post but I was in the post when I came up with the idea.

So, I present to you today, Moderator Scanner! What does it do exactly? It basically just goes thru all the children in workspace to determine whether or not your objects’ names are cool with Roblox or not.

It also does go thru StarterGui and checks the Text property with the same custom filter.

I’ve been talking about settings, this is how you can change and modify them (without actually going into the ModuleScript and modifying the physical table). You can require the ModuleScript “ModScanner” and use the "SetProperty" function. For the parameter, you need to provide a table with the setting you want to change and what you want to set the setting to (you can only set it to a boolean / true or false).

Oh by the way, you need to do this in the console because the code in a Script won’t run until you test the game and when it does eventually run, it won’t have access to the plugin and it won’t save cause you’re testing.

```lua
-- example for yall (IN CONSOLE)
local ModScanner = require(path.to.module)
ModScanner:SetProperty({exampleProp
= true, otherProp = false})
--[[ im typing this on my phone
and I legit forgot the names of the
properties that you put in the table
cuz I named them differently from
their actual names in the
“Properties” table in the ModuleScript
lol
]]
```

<br>

Nice, you know understand the way the plugin scans stuff, now I can actually tell you how to use the plugin and its interface (which is pretty simple).

<br>

## Using The Plugin
##### This goes over how to access and use the interface etc


Okay so the first thing you want to do is get the plugin if you haven’t already done so. Then, you’re going to want to add it to your plugins (Plugins Tab → Manage Plugins → The Plus Sign "+" → The Inventory Icon → My Plugins → Click "Moderator Scanner").

Roblox may warn you about my plugin injecting scripts. I have reviewed my code and there is nothing that is injecting scripts, you can go through it and check for yourself. You may have to enable the “Allow Script Injection” option for my plugin in order for it to function properly.

Click the plugin icon and boom, now you’ve opened the plugin’s interface (its DockWidgetPluginGui)! Now click "Start Scan" to begin scanning your game’s objects! If you don’t want to continue scanning for some reason, you can click “Stop Scan” to terminate the active scan (it will completely stop the scan which means that it won’t get to scanning other stuff and adding an issue which I talk about after this section).

Now I will talk about the final part of this README file, Issues. If the plugin detects that one of your objects’ names or your objects’ text have a banned word in it, it will create a UI element under the “Issues” TextLabel in the plugin’s interface. It will disappear if you change the name or text to something not banned OR the object gets deleted.

<br>

## Plans For The Future
##### Yay I have to come back to this plugin in the future smh (jk)

<br>

You can find this on my Devforum post since this is subject to change
