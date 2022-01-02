This is modified source code for the firmware for the [Tidbit](https://nullbits.co/tidbit/) where Bongo Cat is ported over.
Used code from the oledpet firmware for WPM function as well as the [Nibble](https://nullbits.co/nibble/)'s version of the Bongo Cat firmware.
I'm uploading this because no one else seems to have uploaded the hex or source code.

This is intended to be used with an OLED relocation mounted horizontally to the top right as shown in the images below. (note the mounting requires wiring as the pinouts aren't the same as if you were to mount the oled vertically over the microcontroller, see images below)

If you mounted it from a different location and it is flipped, change "OLED_ROTATION_90" to "OLED_ROTATION_270" in line 82 in keymap.c and recompile:

`oled_rotation_t oled_init_user(oled_rotation_t rotation) { return OLED_ROTATION_90; }`

To compile, use the following:

qmk compile -kb nullbitsco/tidbit -km bongocat

![Diagram](https://i.imgur.com/OlcSDRz.png)
![Working Image](https://i.imgur.com/4m8wOdm.jpg)