## About

This is a Buildroot external tree for the OS of the MMX VESC motor controller.

## Prerequisites

Prerequisites for buildroot [https://buildroot.org/downloads/manual/manual.html#requirement-mandatory]()

## Getting started

Clone the repository

```
git clone git@github.com:Wintergatan/vesc-os.git
cd vesc-os
git submodule update --init
cd buildroot
```

To build:

```
make BR2_EXTERNAL=../ vesc_rpi4_defconfig
make BR2_EXTERNAL=../
```

Use the option `BR2_JLEVEL=<number>` to set the `J=<number>` for make. Then wait...

The generated image will be in `output/images/sdcard.img`. To write the image to the SD card, use:

```
sudo dd if=output/image/sdcard.img of=/dev/mmcblk0
```

Based on [mendeleevos](https://github.com/area3001/mendeleevos).
