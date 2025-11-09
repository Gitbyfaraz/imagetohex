# imagetohex
Converts png file to hex text file, 3 channel 8 bit colour per pixel. Written in C using SDL2

Compiling
Linux - After updating your system run 
sudo apt install libsdl2-dev libsdl2-image-dev
This will also automatically install other dependancies. Then use make.

Windows - No need to install SDL2 as headers and libs/dlls already provided, just clone the repository and run mingw32-make.
Run mingw32-make BUILD=monolithic for static build. Note that for dynamic builds, SDL2.dll and SDL2_image.dll need to be present in the same directory as executablea at runtime.

Usage
When not launched from console, the binary will automatically search for "img.png" in the same directiory as the binary.
When launched from console, an optional filename along with path can be provided. For example:
./imgtohex /path/to/image.png or ./imgtohex Untitled.png etc
Upon exiting, a plain text pixels.mem file will be created in the same directory as the binary. The file contains space separated raw pixel data with each segment in 0xRRGGBB format and a newline every 8 pixels.

The icon on Windows can also be changed by changing the ico file in src/res.
