# Development Journal – ResistorIQ

## November 6, 2026 – Project concept and design
## 30 Min
Started developing an idea for the Hack Club 8-Pin Grant. I wanted to make something practical that I could use in electronics projects, rather than just making another basic microcontroller project.

I decided to make a resistor measurement tool called ResistorIQ. The idea is to let someone insert an unknown resistor, select a reference resistor using a rotary switch, and have the device calculate and display the resistance.

I chose the ATtiny412 because the grant focuses on projects using 8-pin microcontrollers. I also decided to use a 16x2 I2C LCD so the measurements could be displayed without needing a computer.

For the reference resistors, I settled on 1k, 10k, 100k, and 1M ohm values. This gives the device several measurement ranges instead of relying on just one reference resistor.

## November 6, 2026 – Component selection and circuit planning
## 30 Min
Worked on figuring out which components would be needed and finding actual parts that could be ordered.

Selected the ATtiny412 in a SOIC-8 package, along with the four reference resistors and the additional resistors needed for the circuit. I also selected a rotary switch, USB-C power connector, and connectors for the LCD and resistor being measured.

I wanted the PCB to be compact, so I paid attention to component packages and connector sizes when choosing parts.

I also started working through how everything would connect to the microcontroller, including the measurement circuit, display, power, and programming connections.

## November 7-8, 2026 Designing the Schematic
## 2 Hr 35 Min
I started working on the schematic and laying out the connections between parts with the $35 budget in mind.

## November 8, 10, 2026 Routing PCB
## 2 Hr 30 Min

I was trying to learn how to actually do it while doing it and so it took longer than I was expecting but I learned a lot and I finished it after a bunch of googling.

## November 11-12, 2026 – Rebuilding the KiCad project
## 2 hr
Had to spend time rebuilding the KiCad project after losing the previous local project files. This meant recreating parts of the schematic and PCB rather than just continuing from where I left off.

Thankfully this didn't take very long as I knew what to do and also the main idea of the schematic. I rebuilt the schematic and the pcb and started saving everything to github so it wouldn't happen again. I also managed to shrink the footprint even smaller after this to a footprint of 30mm by 30mm. (it used to be like 100mm by 100mm).

One of the more difficult parts was getting the correct footprint for the rotary switch. The switch did not have a suitable footprint readily available, so I had to work on creating and setting up a custom footprint library.

## November 11, 2026 – Custom rotary switch footprint
## 15 Min
Worked on the footprint for the Alpha rotary switch (SR10010F-0204-20F0B-C7-N-0027).

Created the custom footprint file and added it to a footprint library in KiCad. I also had to get the library recognized by the project so that the footprint could actually be selected in the footprint browser.

After some troubleshooting, I got the custom footprint showing up correctly in KiCad and was able to assign it to the rotary switch.

This was an important step because the switch is one of the main parts of the measurement system.


## November 12, 2026 – Bill of materials
## 15 Min
Worked on putting together the final bill of materials. I wanted to have actual manufacturer part numbers rather than just generic component descriptions so the parts could be ordered.

Added the components, quantities, manufacturers, part numbers, and other details to the BOM.

I also researched component pricing and checked whether the selected parts would fit within the $35 grant budget. Some parts were harder to find individually, especially certain passive components, so I had to look at alternative purchasing options.

Created the BOM in Excel and also prepared CSV and PDF versions for the GitHub repository.

## November 12, 2026 – Manufacturing files
## 10 Min
Worked on preparing the PCB for manufacturing.

Set up the Gerber export in KiCad and selected the copper, solder mask, and board outline layers. Also generated the drill files needed to manufacture the holes in the PCB.

The goal was to have the files ready to send to a PCB manufacturer rather than only having a design that could be viewed inside KiCad.

## November 12, 2026 – GitHub and documentation
## 10 Min
Started organizing the project repository so that the design files and other project information would all be available in one place.

Uploaded the KiCad project files, including the schematic and PCB, along with the custom rotary switch footprint. Also added the BOM and manufacturing files.

Started writing the README and development journal to explain what ResistorIQ does and document the work that went into designing it.

## Next steps

The PCB design and manufacturing files are prepared, but the physical device still needs to be built and tested.

My next steps are to get the boards manufactured, assemble the components, program the ATtiny412, and test the measurement circuit with different resistor values.

I also need to check the accuracy of the measurements and make any changes necessary if something does not work as expected.


## Total Time: 8 Hrs 55 Min
