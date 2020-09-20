# Atari XE C25953 emmu unit replicated in GAL16v8 and GAL20v10

As the happy owner of an Atari 65XE I wanted to upgrade and have fun with full 130kB of RAM. After browsing the internet I learned that C25953 is very hard to find. There are some GAL implementations, however those require an extra D latch. Unfortunately my motherboard doesn't support such solution.
As a purist my goal was to stick as close as possible to the original ATARI's design so solutions like 1MB extensions were out of the question. 

After qick investigation, looking into C25953 discreet IC implementation's schematic, it turned out that it's possible to fully replicate C25953 logic within cheap, old, yet still available GALs (GAL16v8 and GAL20v10). The only trick was to generate the missing latched HALT signal used in logic equations.
Unfortunately due to the GALs' hardware restrictions 1:1 pin compatible replica was not feasiblie forcing external wirings.

## Structure of the repository
  - gal16v8 - best to use with a custom PCB:
    - winculp - implementation in CUPL, jedec files, etc. 
    - graphics - photos of the implementation
    - kicad - kicad schematics/pcb and gerber files

  - gal22v10 - can be directly mounted in the socket, however requires some basic wiring and soldering on top of the IC:
    - winculp - implementation in CUPL, jedec files, etc.
    - graphics - photos of the implementation and wiring diagrams  

## Test result with "Video Blitz" demo

![Video Blitz](https://raw.githubusercontent.com/mikulski-lab/C25953-emmu/master/gal16v8/graphics/video_blitz_128k.jpg)
