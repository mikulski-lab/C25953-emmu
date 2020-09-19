# Atari XE C25953 emmu unit replicated in GAL16v8 and GAL20v10

As the happy owner of an Atari 65XE I wanted to upgrade and have fun with full 130kB of RAM. After browsing the internet I learned that C25953 is very hard to find. There are some GAL implementations, however those require an extra D latch. Unfortunately my motherboard doesn't support such solution.
As a purist my goal was to stick as close as possible to the original ATARI's design so solutions like 1MB extensions were out of the question. 

After qick investigation, looking into C25953 discreet IC implementation's schematics, it turned out that it's possible to fully replicate C25953 functionality within cheap, old, yet still available GALs: GAL16v8 and GAL20v10.
The trick was to generate the missing LHALT signal. Unfortunately due to the GALs' hardware restrictions 1:1 pin compatible replica was not feasiblie.

# In the repository I provide two implementations
  - GAL16v8 - best to use with a custom PCB:
    - winculp - implementation in CUPL, jedec files, etc. 
    - graphics - photos of the implementation
    - kicad - kicad schematics/pcb and gerber files

  - GAL22v10 - can be directly mounted in the socket, however requires some basic wiring and soldering on top of the IC:
    - winculp - implementation in CUPL, jedec files, etc.
    - graphics - photos of the implementation and wiring diagrams  
