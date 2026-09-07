---
title: "BLE Keypad"
collection:
    - projects
excerpt_separator: <!--more-->
header:
    teaser: "/assets/images/blekeypad.JPG"
date: 2022-01-01 01:01:01
#  - Blog
#tags:
#  - Post Formats
#  - notice
---

BLE keypad based on the NRF52840 wireless SoC (2022)

<!--more-->

![Image](/assets/images/blekeypad.JPG)

This is the second revision of a wireless keypad based on the NRF52840 microcontroller. It uses a handful of dual-diode packages to form a scanning matrix such that the microcontroller can read all keys with only a few GPIO. To extend the life of the 150mAh battery, all matrix columns are held high during periods of inactivity and scanning only starts when any row see a keypress. This revision also includes an encoder with push-button and I2C EEPROM for storing different key layouts, swappable with a small tactile switch on the side.

The first revision used an interrupt per key as the NRF52840 has plenty of IO for it, which is both simpler to implement in firmware and lower power. The idea for revision two was to create a set of firmware that could be expanded to larger keyboards using the same microcontroller and firmware architecture.
