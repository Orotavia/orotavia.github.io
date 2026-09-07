---
title: "deej Audio Controller"
collection:
    - projects
excerpt_separator: <!--more-->
#categories:
#  - Blog
#tags:
#  - Post Formats
#  - notice
---

deej nuts

<!--more-->

'deej' is a piece of open-source software written by GitHub user omriharel.

https://github.com/omriharel/deej

It allows a user to control the volume of individual applications in Windows over a serial interface (usually through USB). Each channel controls one or more applications as configured by a YAML file.

By using rotary encoders, which are read into the microcontroller with interrupts, I am able to control the volume in user-defined steps. Due to the encoders being incremental as oppose to absolute, the values of each channel are saved to EEPROM after a configurable delay. This is done only when no change is seen in several seconds so as to avoid unnecessary wear of the EEPROM.

The user can interrupt the stream of channel volumes with input from a serial terminal in order to configure a number of parameters through UART commands. 

**Info Notice:** Lorem ipsum dolor sit amet, [consectetur adipiscing elit](#). Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.
{: .notice--info}