---
title: "deej Audio Controller"
collection:
    - projects
excerpt_separator: <!--more-->
header:
    teaser: "/assets/images/deej_cropped.jpg"
date: 2020-01-01 01:01:01
#categories:
#  - Blog
#tags:
#  - Post Formats
#  - notice
---

Custom hardware for per-application volume control (2020)

<!--more-->

'deej' is a piece of open-source software written by omriharel (https://github.com/omriharel/deej). It allows a user to control the volume of individual applications in Windows over a serial interface (usually through USB). Each channel controls one or more applications as configured by a YAML file.

![Image](/assets/images/deej_gif.gif)

My custom version of the hardware uses rotary encoders, which are read by the microcontroller with interrupts, controlling volume in user-defined steps. Due to the encoders being incremental as opposed to absolute, the values of each channel are saved to EEPROM after a configurable delay. This is done only when no change is seen in several seconds so as to avoid unnecessary wear of the EEPROM.

The user can interrupt the stream of channel volumes with input from a serial terminal in order to configure a number of parameters through UART commands. 

![Image](/assets/images/deej_apart.jpg)

**How economical!** The PCB was designed for single-side assembly, both for ease of soldering AND to be able to use the back as a face plate.
{: .notice--info}