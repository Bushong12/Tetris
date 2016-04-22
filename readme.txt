
The 5th version of gfx has 2 new functions, and detects more events.

What's new in gfx5:

 - you can now clear an area of the display with the gfx_clearea function

 - you can change the cursor (mouse pointer) with the gfx_changecursor function
    see the file /usr/include/X11/cursorfont.h for possible cursors 

 - the gfx_event_waiting returns the following values based on various events:
    1 :  for a key press
    2 :  for a key release
    3 :  for a mouse click
    4 :  for a mouse release
    5 :  for a mouse motion
   note that while gfx_event_waiting detects one of the above events 
    (and it still returns 0 for no event), the gfx_wait function can still
    be used to identify which key or which mouse button was used.

The testing5.c file tests the above, and allows you "draw" with a "pen" of
various thickness.  Refer to the program's comments to see how it works.
Note that the pen will not be continuous if the mouse moves fast (feel free
to make the pen continuous, it's an easy fix).

enjoy!
RKB

