# How to use Steam Remote Play with Pokemon Infinity

## Caveats and Acknowledgements (Linux and especially Mac users should read!)
This tutorial works for Linux (need flatpak though) and Windows users. Valve and WineHq has a put a lot of effort in to make pretty much any game or .exe run on linux or mac. I know a suprising amount of the user base for this game comes from mac; however, macOS currently does not support remote play well so while you can run the base game, streaming is not really an option. You would need either a Linux or windows virtual machine to accomplish that (linux might be better since its lighter so you can expect less lag) or some other streaming tool. I guess you could also try installing linux on a mac but I'm not sure what kind of performance you would get especially on M1. Something like Podman for a vm or Parsec for streaming could suit your needs. If you use mac or linux as your host machine and no longer want to try this, just follow the pinned tutorial for running the game under wine in #bug-reports.
<br/><br/>
Just as a little disclaimer, I personally use linux so this tutorial is coming from that perspective though that should have no impact on a windows user. The tutorial is slightly more complex on linux but if you are using windows you can just skip those sections.

## Downloads 
Download the game from #downloads in the discord onto the host machine and unzip the file wherever you want it (make sure you you remember where you put it! We'll need it for steam later). <br/>

Download Steam onto the host machine: https://store.steampowered.com/ <br/>

Download Steam Link onto wherever you are streaming to (All platforms are supported): https://store.steampowered.com/remoteplay#anywhere

## Steam Setup (This is all done on the host machine!)

Open Steam and click on Add New Game in the bottom left-hand corner.

![add-game](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/add-game.png)

Then click add non-steam game.

![non-steam](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/non-steam.png)

Click Browse and navigate the directory with that has Pokemon Infinity installed. It should look like this after navigation:

![select-game](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/select-game.png)

Click on Game.exe and click open. Then click add selected programs. If everything was done correctly, you should have Pokemon Infinity in your library!

But it shows up as Game.exe and not Pokemon Infinity, let's change that. Click on the new shortcut "Game.exe".
You can right click on the black background to change the logo and backdrop. I have mine setup like this (you can the logo I used [here](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/pokemon-infinity.png) and the background [here](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/splash.png)):

![setup-splash](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/setup-splash.png)

You are also going to want to change the direct shortcut name and logo. Click on the application and the gear on the right-hand side near the center of the screen. Then click on properties.

![gear](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/big-gear.png)

This should open the shortcut properties menu. Change the name and then click on the blank square and set the image whatever you like (I have mine to set to the logo from earlier). Final result:

![setup-shortcut](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/setup-shortcut.png)

At this point the game should be runnable on both windows and linux. However some more setup is needed on the linux side of things to make the game fully work. If you are on windows skip the next section and go to client side configuration.

## Linux and Linux VM Steam Setup
The game does not run by default under steam proton. You need to enable steam play for other titles. Click on settings in the top-left and then click steam play and check enable steam play for other titles (use the default it puts there). 

Then you need to download protontricks to configure proton for Pokemon Infinity (make sure you run the game once before continuing, the game will work but it will crash once you start a new game). The easiest way to get protontricks is through flathub [here](https://flathub.org/apps/details/com.github.Matoking.protontricks) or you can find it on github [here](https://github.com/Matoking/protontricks). 

Open protontricks and select Pokemon Infinity, it might bring up some menus warning you about a 64-bit wine prefix but click ok and ignore that. Once the main window pops up click select default wineprefix and then click install a windows dll or component. Scroll down to gmdls and check it then click ok. The General MIDI DLS collection is now installed and the game should work perfectly.

## Client Side Configuration and Controller Setup
This step may differ depending on what you are streaming to and what controller you are using, so I am not going to say explicity what keybinds to use. I'm just going to share where changes need to be made if you want something different and what my setup looks like.

Boot up Steam Link on your client device (I'm using my iPhone for this) and pair it with the host machine. Once you are setup connect and start playing.
Navigate to the gear in the top right-hand corner and select it (This should be "A" depending on your controller):

![big-gear](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/big-gear.png)

Then navigate to Base Configurations and select it:

![base-config](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/base-config.png)

Then navigate to Desktop configuration and select it:

![desktop-config](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/desktop-config.png)

Setup up your configuration however you like in here. Mine looks like this:

![final-showing](https://raw.githubusercontent.com/TeryVeneno/pokemon-infinity-remote-play/main/images/final-showing.png)

And there you go, you should be all set up. Start Playing and Remember to Have fun! 
