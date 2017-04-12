[__NEWS__](NEWS.md) | [__TODO__](TODO.md)

-----------------------------------------------------------------------

Looks like EmuState is past around to control the emulator Which is a structure of ```SystemState```

```SystemState EmuState;```

For the Aspect Ratio the relevant members are initialized to 

```
EmuState.WindowSize.x = 640;
EmuState.WindowSize.y = 480;
```
And I don’t see where they get reset anywhere … 

Does this mean that regardless the size of the VCC window, DirectDraw is dealing is shrinking or stretching a 640x480 surface? 

We Create a DirectDraw Window in -> ```CreateDDWindow(SystemState *CWState)``` 
once on init and then each time we toggle from fullscreen mode to windowed mode

We create our main window ... 

The Window is adjusted to keep the "Client Rectangle" still at 640x480

The status bar is created and again Window is resized to keep the "Client Rectangle" still at 640x480

We then initialize DirectDraw (g_pDD)
Create our Primary Surface (g_pDDS)
Create our Back Surface (g_pDDSBack)

And again the Back Surface size is also at 640x480
```
ddsd.dwWidth  = CWState->WindowSize.x; // Make our off-screen surface 
ddsd.dwHeight = CWState->WindowSize.y;
```
Then we create a Clipper (g_pClipper)
Assign our Main Window's HWND to it
Attach the clipper to the primary surface

Lastly, it looks like we Test the Back Surface by locking and unlocking it ... 

---- 

Now the question is, what happens to these and the main Window when resized? 
I don't see anywhere the Main window is responding to WM_SIZE 

hmmm ...

I think the key will be here ```DisplayFlip(SystemState *DFState) // Double buffering flip```

It's the only place where the Back Surface is drawn onto the primary
basically our Client Rectangle ... 

```
hr = g_pDDS->Blt(&rcDest, g_pDDSBack, &rcSrc, DDBLT_WAIT , NULL); // DDBLT_WAIT
```

where rcSrc ==> 0, 0, DFState->WindowSize.x, DFState->WindowSize.y 
which is the size of our Back Surface (which I'm pretty sure is always 640x480)

and rcDest ==> the client rectangle transformed into SCREEN coords --> left,top - right,bottom  minus the status bar 

ahh... Since our client rectangle can be any size the BLIT streaches 

I'm close ... 

-----------------------------------------------------------------------

There are 4650 occurrences of 'PTRsurface' in 3 files.
```
unsigned char	*PTRsurface8;
unsigned short	*PTRsurface16;
unsigned int	*PTRsurface32;
```
Obviously, they must play an important role in the rendering process!!! study what they do ... 

