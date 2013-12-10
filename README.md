### Unreal Tournament 2004 under Linux - FAQ

- Q. How to install?

 A. Browse to your DVD contents then `sh linux-installer.sh`

- Q. How to run?

 A. Browse to your installation path then `./ut2004`

- Q. _./ut2004-bin: error while loading shared libraries: libstdc++.so.5: cannot open shared object file: No such file or directory_

 A. `yum install compat-libstdc++-33`

- Q. No sound (with PulseAudio)

 A. `padsp ./ut2004` instead of `./ut2004`

- Q. Can't select resolution higher than 1280x800

 A. `vim ~/.ut2004/System/UT2004.ini` and update the lines `FullscreenViewportX=1600` and `FullscreenViewportY=900`

- Q. Use Nvdia card with Optimus

 A. `DRI_PRIME=1 padsp ./ut2004` (`DRI_PRIME=1 glxinfo | grep "OpenGL vendor string"` should say "nouveau")

- Q. Can I play using the integrated Intel GPU, i.e. without `DRI_PRIME=1`?

 A. Yes with default display settings. But I get a segfault with higher settings.

- Q. The game crashes with _Assertion failed: p->model1 [File:KFarfield.cpp] [Line: 937]_

 A. You're running the retail release (build 3186). You need to upgrade to build 3204. But it's probably a better idea to apply the [megapack](./mega_pack.txt) patch which includes many other fixes and improvements.

- Q. _./System/ut2004-bin: error while loading shared libraries: ./libSDL-1.2.so.0: cannot open shared object file: No such file or directory_

 A. `cd System && ./ut2004-bin`

- Q. How do I get UnrealEd (the maps editor)?

 A. You can't :( (see http://openut.sourceforge.net/edit.php)

- Q. Hotkeys don't work / Alt-Tab doesn't work

 A. It's because SDL grabs the whole keyboard - you can use [my fork](https://github.com/infertux/SDL-1.2.7/tree/allow_alt-tab) to get Alt-Tab back.

- Q. Anything else?

 A. Don't forget to crank up the display settings to _High_/_Highest_ and set the bots level to _Godlike_ for a better experience! Enjoy ;)

