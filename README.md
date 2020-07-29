Based of https://github.com/ptitSeb/OpenArenaPandora

I have modified the EGL code to run with GBM so that X11 is no longer required.
To enable this, pass ROCK at compile time.

OpenArena
================
OpenArena version for ROCKCHIP / OpenPandora / ODroid / RPi, featuring ARM support and GLES renderer.

The current state is playable without any major problems and good performances. 
Only limits are len flares that requires depth buffer reading and so are disabled.
Note that this version integrate a QVM with a JIT backend on ARM, so bots doesn't slow down the games too much.

OpenPandora / ODroid / RPi
===========

This version is aimed at OpenPandra, so get:
 * ARM compatibilty (using -DARM)
 * Some NEON optimized code (using -DNEON)
 * GLES renderer (using -DHAVE_GLES)
 * Toggle Crouch function (using -DCROUCH), disabled by default and with a new option in cfg
 * OpenPandora support of course (using `-DPANDORA`), for screen resolution mainly.
 * ODROID support (build with `make ODROID=1`), mostly like Pandora, but without the control and resolution hack
 * RPI support (build with `make RPI=1`), same as ODROID (will not work for RPI 1, has NEON support is compiled in)


There are some hard-coded value in the Makefile, located at the beggining to force "OpenPandora version" (`COMPILE_PLATFORM=pandora` and `COMPILE_ARCH=arm`, and that are used for Pandora, ODroid and RPI build).
 
Note that RPI build is untested, any feed back is welcome.

For more info on the OpenPandora go here: http://boards.openpandora.org/
Specific thread for Jedi Academy on the OpenPandora here: http://boards.openpandora.org/index.php/topic/13695-open-arena/
