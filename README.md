# “*VCC-Classic*”

I am slowly building up steam to work on this thing. I’ve been wanting to for a long time but have NOT had the time.  Well, I still don’t.  But I am just going to make the time. If you are reading this, don’t expect a lot of progress fast. 

My plan for this “fork” is NOT to attempt to make VCC multi-platform (Windows/Mac/Linux).  But to, instead make improvements and maintain the current code-base as is, and keep it Windows only; a “VCC-Classic” if you will. 

Along those lines, I am also NOT interested in changing it to only compile on the latest Dev tools, like VS2015 (or now VS2017).  In fact, I would like to maintain the ability to compile it with VS 6.0. Back around July 2016 I clean-up some of the VS6 files and got it to compile/build. 

If I am NOT mistaken, it’s possible that VCC (like 1.42) might have been compatible w/ even Windows 98. To me, It would be interesting to see it remain so. 

There is NO reason to update the code so that it only compiles under the new Dev tools. The DirectDraw technology that VCC uses, is already outdated. "*DirectDraw has been deprecated since version 7*".  Which I believe dates back to Windows 98 timeframe anyway.  Updating the Dev Tools does not change this fact. 

With that said, I will, however, look at adding “back” the capability of compiling/building it w/ newer versions of VS (including 15/17), but just not those exclusively. And it looks like that Mark McDougall has already done the work to get it to compile w/ mingw64.   

### My TODO – list of priorities. 
* Study the code and begin making some notes on it -- put the notes in *.md files 
* ~~Locate my last changes from 6/2016 and sync w/ this baseline.~~ 4/10/17 
* First thing is find and fix the aspect ratio. And make that the default. That thing bugs me to no end. 
* Then add some standard zooms line 1x 1.5x 2x … (the 1x & 2x … are ideal, because then they are pixel perfect)
* Next would be to refresh a ROM file and reset CPU when a file change occurs, for quick development of ROMs (also look at doing the same thing for DSK files (and .bin? files)
* Add a ToolBar, that is dockable, w/ the most frequent settings.  
* Look over the issues list on the VCC site.

--------------------------------------------------------------------------------

**4/11/17**: Ok... this thing is back to compiling/building using VS6 (with the last good service pack SP6). This has all the latest changes to VCC-1.200b including Mark McDougall’s changes (msmcdoug branch) that allow it to compile using MinGW-w64, minus his “profiling code” which VS6 cannot compile. (TODO: link to notes on that issue here)

It includes one change --> changed all the dialog boxes to use Tahoma 10pt font – this is a much better looking font that the default MS Sans Serif 8pt.   

----- Edit Bellow -----

### Compiling The VCC Sources

Currently, VCC is compiled in C/C++ using "Microsoft Visual Studio 2015 Community", which is a free download from the MSDN downloads. When downloading VS2015, you must make sure to get the Win32 and WinXP compatibility packages to ensure build compatibility with older versions of Windows.

VS2015 requires Windows 7 or greater to install. Check the VS2015 "System Requirements" before trying to install on your system.

As of the current build, there are no "extras" needed to compile VCC. This may change at any time as we are trying to eventually move the code to cross-compile for cross-platform use, making VCC available for Mac and Linux users and not just the Windows users.

Compiling any VCC sources other than the "Release" source set is not guaranteed. Any branch other than the release may at any time, be in a state of developement in which it is not compilable as we are constantly updating the sources with changes. We will try to maintain the default branch as the "Release" branch ensuring a "running" emulator. For example; the "Original Masters" branch is a copy of Joseph Forgeone's (VCC's original author) original "VS C++ 6" code that when using that platform, will compile into the equivelent of VCC 1.42. It WILL NOT compile under VS2015. These sources are stored here more for historical purposes than anything else.

We welcome all bug reports and suggestions. Post any bug reports and/or suggestions on the "Issues" page and we will be promptly notified. We do a "check list" of the issues page every-so-often to see if there's any "quick fixes" we can add while we are working on current changes. The VCC Developement Team is a small one and we work on this when we can as we all have lives and families, so VCC is NOT a priority but a hobby. Even being a hobby, it is also a work of love as we also use this software ourselves, so we try to make it as usable as possible. Sometimes progress is slow and it looks like nothing is going on (and it may not be), but usually, there's plenty going on behind the scenes and we have not committed our current work. Progress is slow, but progress is being made.

If you think you have patches or code that could contribute to the VCC project, please contact the developement team and we will see if it fits the current direction of the project, and if so, add it to our code. Be sure to add your name and the date in your comments (and please comment your code well) if you want credit for your work. Also, if your programming skills are up to "snuff" and you feel you would like to join the VCC project, contact us and we will see if you are worthy :-)

We will continue to try to make VCC the best Color Computer Emulator available.

Thank You for using VCC

The VCC Developement Team.