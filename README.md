# Plasma
Basic HTML website to convert mastercam .NC export files to work with a plasma cutter.

## What does the algorithm do?
This is a personal project, that I decided to release. This search and inserts some GCode into a provided .NC file, which should have come from MasterCam because of the specific things it looks for, however, you can modify it to work with other programs if you'd like. Out of the box, plasma will search and replace for lines that contain ``G0 Z1``. These lines will be replace with
```gcode
G31 Z -100 F19.685
G92 Z-0.04
G00 Z0.1500
M03
G04 P0.4
```
*note: the line numbers are reconciled after; these are the commands sub Nx*

### Will this work for you?
Probably not. I have very superficial knowledge about the machines this is made for, I don't even know the name of the plasma cutter that we use. I was given direction on how to design the algorithm by a machining instructor, for whom this code is for.
If you do decide to use this for your machines make sure to do some tests, run an example .NC file through and make sure that in multiple places the output is what you'd expect. If your machine is damaged or you lose a part due to this, I am NOT responsible. A warning similar to this will be appended to the output after every successful output. Please read the warnings!!
