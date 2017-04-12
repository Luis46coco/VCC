# “*VCC-Classic*”

[__NEWS__](docs/NEWS.md) | [__TODO__](docs/TODO.md) | [__NOTES__](docs/NOTES.md)

I am slowly building up steam to work on this thing. I’ve been wanting to for a long time but have NOT had the time.  Well, I still don’t.  But I am just going to make the time. If you are reading this, don’t expect a lot of progress fast. 

My plan for this “fork” is NOT to attempt to make VCC multi-platform (Windows/Mac/Linux).  But to, instead make improvements and maintain the current code-base as is, and keep it Windows only; a “VCC-Classic” if you will. 

Along those lines, I am also NOT interested in changing it to only compile on the latest Dev tools, like VS2015 (or now VS2017).  In fact, I would like to maintain the ability to compile it with VS 6.0. Back around July 2016 I cleaned-up some of the VS6 files and got it to compile/build. If I am NOT mistaken, it’s possible that VCC (like 1.42) might have been compatible w/ even Windows 98. To me, It would be interesting to see it remain so. 

There is NO reason to update the code so that it only compiles under the new Dev tools. The DirectDraw technology that VCC uses, is already outdated. "*DirectDraw has been deprecated since version 7*".  Which I believe dates back to Windows 98 timeframe anyway.  Updating the Dev Tools does not change this fact. 

With that said, I will, however, look at adding “back” the capability of compiling/building it w/ newer versions of VS (including VS2015/VS2017), but just not those exclusively. And it looks like that Mark McDougall has already done the work to get it to compile w/ MinGW-w64.

#### Compiling The VCC Sources

If using VS6 -- open Vcc.dsw and build. 

TODO: Will put further instructions here later ...

#### VCC is NOT a priority but a hobby. 

It's also a work of love! However, most likely, progress will be slow, but hopefully, progress will be made. 

We welcome all bug reports and suggestions. Post any bug reports and/or suggestions on the "Issues" page. 

If you would like to contribute to the VCC project, then learn Git & GitHub, fork the branch of your choosing and hack away. If you would like to help me on this particular VCC-Classic fork then by all means start your fork from jross9/VCC and let’s learn how to collaborate in the open – since this is, after-all, open-source. Right?
