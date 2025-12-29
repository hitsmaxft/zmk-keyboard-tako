# zmk keyboard module for Tako EC

This repository contains the ZMK configuration for the Tako split keyboard with EC (Elite-C) controllers.

## Calibration

The first thing you should do after assembling the keyboard is to calibrate the matrix.

You should be able to access ZMK logs through the console. See [ZMK docs](https://zmk.dev/docs/development/usb-logging) for details.

Next, you should adjust actuation and release values for each key in the `tako_drivers/kscan/kscan_gpio_ec.c` file. Basically, actuation should happen at the tactile bump, but you can prefer different levels depending on your typing style. If the key actuates too early, then increase the value in the `actuation_threshold`. If it's too late, then decrease it. After this is done, you should change the `release_threshold` to reflect the actuation change – reducing it by 50 should work great.

Don't map actuation levels too close to base reads (what you see in console when no touching keys).

## Install Guide

1. Add this repository as a module to your ZMK config
2. Enable the Tako shield in your build configuration
3. Configure the left and right halves according to your hardware setup
4. Calibrate the keyboard matrix as described above

## Update Notes

* Migrate to standard ZMK external module structure
* Add ZMK Studio support for easier configuration
* Update device tree configuration for better hardware support
* Enable pointing device support
* Improve ADC configuration for more accurate key readings
