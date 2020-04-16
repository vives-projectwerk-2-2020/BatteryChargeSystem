# Battery charge system

## Project description

The concept of the this system is to charge some batteries with a solar panel. To supply the whole system.

## Explanation of my roadmap

I first started with the development boards for charging 1 battery with a solar panel. I had 3 boards for use. So I picked the right one. The Adafruit pcb was very interesting for me. And like we all know a Li- Ion battery must be protected when it's fully charged.
After testing everything on the dev pcb's I started designing my own PCB. I used the Eagle software because we're used to it. It wasn't difficult to find the schematics of the dev PCBs. I used those schematics for my base to draw my own PCB.

## problems

I hadn't any problems with the PCB draw. Only needed some research for the GND polygoon.

The first problem that came in the game was the Covid-19 outbreak. No more lessons, no more contact with other students. So it wasn't easy to trade the components between some students.

The second problem was that the pcb got down after 3 minutes. When there was no battery attached to the pcb the system worked fine. But once attached, after three minutes, the PCB shuts down. 
I did some debugging. The problem was some duplicate functionality. The main IC thought that there was a fully charged battery attached. The MCP 73871 haves all functionality build in that is necessary. So I scrached a wire away so the other ICs (LC05111CMT and MCP73833). The 2 MCP's have the same functionality.
So now the PCB works fine and I could reduce the needed space on the PCB to a minimum.

## Resources

I used the datasheet of the MCP73871 for debugging my PCB. The other documentation was found on the internet. Mostly used for designing my own PCB.

## Next steps

The next step is a duration test. To charge a battery full and apply an Arduino.
