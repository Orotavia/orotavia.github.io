---
collection: "test"
title: "Capsized Battleship Game"
collection:
    - projects
excerpt_separator: <!--more-->
header:
    teaser: "/assets/images/capsized_small.png"
date: 2026-01-01 01:01:01
#categories:
#  - Blog
#tags:
#  - Post Formats
#  - notice
---

The classic game of Battleship but more exciting (2026)

<!--more-->

![Image](/assets/images/capsized_small.png)

Created for the 2026 Formlabs Hackathon. I designed the electronics for a version of Battleship in which your shot explodes a reverse-biased electrolytic capacitor on the opponent's ship if you hit. It makes for a pretty nerve-wracking game, not knowing when to expect the pop!

![Image](/assets/images/capsized_ship_small.png)

The design is based around two 10x10 matrices of pogo-pin targets. For any given shot, current is sourced to one column and sinked from one row, allowing us to target individual squares. IO usage is further reduced with 4:16 decoders, with the bonus of being a hardware guarantee that only one square is targeted at a time. At the start of each game, current is reduced while every square is scanned - by monitoring current, we can determine which squares are occupied so we can tailor animations to the game state. 

Two encoders and an enticing red button serve as your means of targeting enemy squares, and an addressable LED screen informs you of hits and misses. 

**Safety!** A polycarbonate shield covers the game board to prevent capacitor shells from becoming projectiles, and exhaust fans with carbon filters help reduce the fumes from evaporated electrolyte. 
{: .notice--warning}
