# PyfaForLinux
This is a bash-shell script to create an [AppImage](https://github.com/AppImage) for [Pyfa](https://github.com/pyfa-org/Pyfa). 

Everything needed to run Pyfa is inside a single file. It should run on any regular Linux distribution. The resulting .appimages were tested on Solus, Ubuntu and Fedora.   

# How to use?
- create a folder for Pyfa, then clone it via: git clone https://github.com/pyfa-org/Pyfa
- Download or copy and paste the contents of the script into a textfile
- put it into the root folder of Pyfa (the one that contains pyfa.py and folder names like gui, scripts, utils)
- make the script executable (e.g. open a terminal, navigate towards Pyfa and do: chmod +x AppImageCreationScript.sh)
- run the script (e.g. in the terminal and inside the Pyfa folder do: ./AppImageCreationScript.sh)
- wait a few minutes until it is completed
- the tickets are now diamonds and the Pyfa folder should contain e.g. a pyfa-v2.9.0-x86_64.appimage file of about 120MB size
- double click or run the file via terminal. Enjoy!

# Pros and Cons
Pros
+ a single file
+ easy to use, easy to remove
+ no root capabilities needed
+ no need to install anything
+ use it basically distro-agnostic
+ works with [Firejail](https://github.com/netblue30/firejail) to help alleviate the trust issue

Cons
- requires trust, if the AppImage is downloaded and used instead of self-created by this open-source script
- it may have some glitches

# Motivation
Quick and dirty: the dependency-hell brought me to this point. Every time I updated Pyfa, it was a major pain fiddling with newly inserted requirements and libraries and subversions of wxpython, using pip to install etc. There were not many alternatives, the Debian version of Pyfa wasn't updated in three years. I've looked at some ideas how to solve this problem once and for all, but solutions like Flatpak, Snap and [pex](https://github.com/pantsbuild/pex) all have their oddities. I wanted AppImage. 

The plan was to use [this roadmap](https://github.com/AppImage/AppImageKit/wiki/Bundling-Python-apps) about how to use AppImage to bundle a Python programme, but it was too sketchy and didn't work at all, and killing the dependencies wasn't exactly easy. So I found me an assassin to get rid of them, and not just any assassin, but [The Assassin](https://github.com/TheAssassin), one of the developers of AppImage, to help with this task. He was so down-to-earth and helpful, that he ended up writing the entire script, I simply delivered the payload, did the testing, error reporting, minor bug-hunting and publishing. All credits for the script lie with him. 

# Known bugs
- upper right corner character display does not show which character is active, but selection and skill application works

# Notes
On a fresh Lubuntu 18.10 installation I had to get libwebkitgtk-3.0.so.0 from the Ubuntu repository

# Happiness
If you want to share your happiness, my ingame name is Halvorsen.
