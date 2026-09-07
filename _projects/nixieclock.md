---
title: "Nixie Clock"
collection:
    - projects
excerpt_separator: <!--more-->
header:
    teaser: "/assets/images/nixie_front.jpg"
#categories:
#  - Blog
#tags:
#  - Post Formats
#  - notice
---

Four digit clock based around the IN-18 Nixie Tube (2019)

<!--more-->

At the heart of this clock is a 12V to 170V boost converter, by which four (very old) IN-18 Nixie tubes are powered. At startup the high voltage 'strikes' the cold filaments, then current starts to flow and the maintaining voltage is reduced by a resistor. 32 filaments are driven by a HV open-drain shift register which interfaces with the AVR MCU via level shifter.

The time is maintained with an RTC with a battery backup (CR2032 coin cell). There is a parser that allows the time, date, and format to be set through UART commands. 

**Safe-ish** HV is also shut off when the presence of a finger is detected by a capacitive 'guard ring' around the front of the clock, and also for several hours in the middle of weekdays to prolong the lifetime of the tubes. It's probably not passing compliance though.
{: .notice--danger}
