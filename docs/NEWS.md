[__TODO__](TODO.md) | [__NOTES__](NOTES.md)

__04/11/17__: -JR
 * Ok... this thing is back to compiling/building using VS6 (with the last good service pack SP6). This has all the latest changes to VCC-1.200b including Mark McDougall’s changes (msmcdoug branch) that allow it to compile using MinGW-w64, minus his “profiling code” which VS6 cannot compile. (TODO: link to notes on that issue here)
 * It includes one change --> changed all the dialog boxes to use Tahoma 10pt font – this is a much better looking font that the default MS Sans Serif 8pt.   

-----------------------------------------------------------------------

Need the aproximate dates/history of how this became open source 

-----------------------------------------------------------------------

These entries came from the original ReadMe.txt file. Entries were presumably made by Joseph Forgione

__06/04/2007__: Fixed Fullscreen and 32bit composite color problem

__07/27/2005__: Rewrote wd1793 code from scratch. Nitro09 "works" now.

__07/18/2005__: 
  * Moved the Roms images internal with option to load from .rom files if needed.
  * Fixed the Tandy demo bouncing ball problem. vpitch wasn't calling SetupScreen()
  * Found the problem with Dungeons of Daggorath!!! lea calculations weren't getting added to the cycle counter this was extending the interupt times as all timing is based on CPU time. 

__07/15/2005__: 
  * Added support for the new interupt model.
  * Gate Crasher demo works.

__07/14/2005__: Hres text now works except blink.

__07/10/2005__: 
  * Got the CC3 graphics rendering engine working
  * Tandy demos now work (sort of)
  * removed mc6847 c & h replaced with GimeGraphics c/h

__06/28/2005__: 
  * Moved Memory access code from mc6809.c to mmu.c
  * renamed io_glue.x to iobus.x
  * general code cleanup where possible.

__06/25/2005__: 
  * Reworked for DirectX and broke the joysticks
  * required massive rewrite of mc6847.c 

__06/24/2005__: Moved source to x86 platform from Poco and changed name to reroc

__04/01/2005__: reorged code a bit

__03/16/2005__: 
  * OS9 fixed (hope) OS9 sends an FDC command before it selects a drive I considered this an error
  * added Drive active "light" to UI
  * ??? canyon climber doesn't work with HS interupt on. ??? timing? 

__03/25/2005__: Canyon climber image was bad. works fine

__03/31/2005__: Joystick works in all 3 modes now full/corner/hardkey

__03/15/2005__: 
  * OS9 Booted!!! But crashes if a dir takes more than a screen of files
  * BUG ADCB_D was changing the A register! DOD works better

__03/14/2005__: Fixed ASR ops

__03/13/2005__: SEX and DAA seem ok now. all CC are getting set. 

__03/11/2005__: ROMS are now internal 

__03/10/2005__: Fixed problem with Keyboard icon showing while emulator is running.

__03/06/2005__: Started playing with sound output code

__03/06/2005__: Began emulating wd1793 FDC

__03/05/2005__: Joystick works

__03/02/2005__: CPU core mostly "works" now.

__02/27/2005__: Emulated RAM/ROM Maps arcanoid works now.

__02/22/2005__: Mega-Bug weird lines fixed leax	a,x is signed!

__02/20/2005__: stellar life line acts funny fixed SEX was using an unsigned B register

__02/14/2005__: 6847 mostly working with gapi now.

__02/10/2005__: Moved from GDI to Gapi

__02/08/2005__: Moved from VS6 to EVC3 CPU deved on a PC for ease of debugging

__02/06/2005__: faking the 6847 but it works sort of

__02/03/2005__: SAM Emulation 

__01/30/2005__: Got enough CPU working to write the keyboard routines and rough 6821 emulation

__01/24/2005__: 10:21:44 PM EST Emulation Core is able to start Extened basic (barely)

__01/18/2005__: Did switch case framework

__01/17/2005__: Began writting 6809 core (Plan09)

__01/15/2005__: Gave up on PC-Dragon , It uses to many "tricks" to work 

__01/12/2005__: Began porting PC-Dragon to windows
