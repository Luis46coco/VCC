# “*VCC-Classic*”

[__NEWS__](NEWS.md) | [__TODO__](TODO.md) | [__NOTES__](docs/NOTES.md)

I am slowly building up steam to work on this thing. I’ve been wanting to for a long time but have NOT had the time.  Well, I still don’t.  But I am just going to make the time. If you are reading this, don’t expect a lot of progress fast. 

My plan for this “fork” is NOT to attempt to make VCC multi-platform (Windows/Mac/Linux).  But to, instead make improvements and maintain the current code-base as is, and keep it Windows only; a “VCC-Classic” if you will. 

Along those lines, I am also NOT interested in changing it to only compile on the latest Dev tools, like VS2015 (or now VS2017).  In fact, I would like to maintain the ability to compile it with VS 6.0. Back around July 2016 I clean-up some of the VS6 files and got it to compile/build. If I am NOT mistaken, it’s possible that VCC (like 1.42) might have been compatible w/ even Windows 98. To me, It would be interesting to see it remain so. 

There is NO reason to update the code so that it only compiles under the new Dev tools. The DirectDraw technology that VCC uses, is already outdated. "*DirectDraw has been deprecated since version 7*".  Which I believe dates back to Windows 98 timeframe anyway.  Updating the Dev Tools does not change this fact. 

With that said, I will, however, look at adding “back” the capability of compiling/building it w/ newer versions of VS (including VS2015/VS2017), but just not those exclusively. And it looks like that Mark McDougall has already done the work to get it to compile w/ MinGW-w64.   

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