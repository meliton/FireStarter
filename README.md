ApzStarter
=========

__ApzStarter is a Non-Root Launcher Replacement / App-Drawer for Amazon FireTV:__

Visit discussion on XDA-Developers: 
 * <a href="http://forum.xda-developers.com/fire-tv/themes-apps/app-root-home-launcher-replacement-app-t3118135" target="_blank">[APP] FireStarter | Non-Root Home Launcher Replacement / App-Drawer for FireTV</a>

### Features:
 
 * Similar to Redth's <a href="https://github.com/Redth/FiredTVLauncher" target="_blank">FiredTVLauncher</a> with __REAL HOME BUTTON CLICK DETECTION__ 
 * (and no "amazon home is top-application"-detection).
 * __Even double-home-clicks are captured!!__
 * Completely configurable which app is started on startup-, home-button-single-click or home-button-double-click.
 * Default: Starts itself on FireTV-Startup.
 * Default: Starts itself when Home-Button is single-clicked.
 * Default: Starts amazon home when Home-Button is double-clicked (actually does nothing as amazon home is the default action for home-button clicks). 
 * You can e.g. start Kodi on double-click and FireStarter on single-click.
 * Also possible is to keep up the default behaviour (" - No Action - ") on a single-click (amazon home is starting) and to open e.g. FireStarter on a double-click.
 * Lists all user-installed apps including sideloaded / adb installed apps.
 * Apps can be easily sorted / ordered by settings-button or click-drag-and-drop (long-click to start drag-and-drop).
 * Apps can be hidden from app drawer (see settings).
 * Kodi and SPMC can be installed and updated directly out of FireStarter (see Updates section).
 * Possibility to change the time of no action the FireTV waits to go to sleep.
 * Possibility to import / export settings.
 * Show system and device informations like Android-Version, Build-Version, Hostname, WiFi- / WLAN Name (SSID), IP Adress and Uptime.
 * Automatic update mechanism.
 * __No root required!__

### Install FireStarter:

__Easy installation in less than 5 minutes with only the FireTV__
 * https://github.com/sphinx02/FireStarter/wiki/Install-FireStarter-and-Kodi-(only-FireTV-needed)

__Standard installation via ADB__
 * If you don't know how to sideload/install apps via ADB, read a tutorial (e.g. <a href="http://kodi.wiki/view/HOW-TO:Install_Kodi_on_Fire_TV" target="_blank">this one</a>)
 * <a href="https://github.com/sphinx02/FireStarter/releases" target="_blank">Download latest FireStarter APK</a> and sideload/install with adb: 
 * _adb install -r FireStarter-v3.2.3.apk_
 * Start FireStarter once with adb (or manual from settings menu): 
 * _adb shell am start -n "de.belu.firestarter/de.belu.firestarter.gui.MainActivity"_
 * ADB-Debugging needs to stay enabled (do not disable ADB-Debugging after installation).
 * Enjoy :)
 

### Changelog:
 * [Check releases page for changelog ..](https://github.com/sphinx02/FireStarter/releases)

### ToDo List:
 * Further GUI optimizations
 * Add better install instructions for users that dont know adb..
 * Perhaps add possiblity to install and keep updated some apps via FireStarter (e.g. Kodi, Es File Explorer, ..)

### Screenshots:


### Why using it and how it works:
 * ApzStarter is for all people who dont want to root (and therefore lose warranty) their FireTV's.
 * On the FireTV, Amazon allows no alternative default launchers and in the default launcher of Amazon, no sideloaded (via adb installed apps) are shown. They have to be started via the FireTV settings menu which is really inconvenient.
 * Solutions currently out there are either using root-rights to replace the home launcher or they are polling the top application in the background and then starting other apps if e.g. the Amazon default launcher is detected.
 * FireStarter uses the fact, that every time the home-button is clicked, there is a special output in the adb logcat log. FireStarter starts a local adb logcat session and waites for this output (which is only working as long adb is enabled in FireTV settings). This approach has the advantage, that the top activity dont has to change to detect a home-button click. FireStarter is therefore even able to detect a double-click and starting any actions on home-button single- or double-clicks.
 * Still not solved is the problem, that the default launcher flashes shortly before the right app is started. The default-behaviour of the home-button can still not be disabled.

### Credentials:

  * [FiredTVLauncher](https://github.com/Redth/FiredTVLauncher) for a lot of brilliant ideas
 * [XDA-User g4rb4g3](http://forum.xda-developers.com/showpost.php?p=56319876&postcount=87) for the home-button detection idea
 
