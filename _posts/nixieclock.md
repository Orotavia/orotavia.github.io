---
title: "Nixie Clock"
collection:
    - projects
#categories:
#  - Blog
#tags:
#  - Post Formats
#  - notice
---

Nixie tube clock

At the heart of this clock is a 12V to 170V boost converter, through which four (very old) IN-18 Nixie tubes are powered. At startup the high voltage 'strikes' the cold filaments, after which current starts to flow and the maintaining voltage is reduced. 32 filaments are driven by a HV open-drain shift register which interfaces with the AVR MCU via level shifter.

The time is maintained with an I2C RTC with a battery backup (CR2032 coin cell). There is a minimal parser that allows the time, date, and format to be set through UART commands. The HV is shut off for several hours in the middle of weekdays to prolong the lifetime of the tubes. HV is also shut off when the presence of a finger is detected by a capacitive 'guard ring' around the front of the clock.

**Info Notice:** Lorem ipsum dolor sit amet, [consectetur adipiscing elit](#). Integer nec odio. Praesent libero. Sed cursus ante dapibus diam. Sed nisi. Nulla quis sem at nibh elementum imperdiet.
{: .notice--info}