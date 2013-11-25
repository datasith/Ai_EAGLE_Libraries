Overview
---
This repository includes our libraries for [CadSoft EAGLE PCB Design Software][1] (version 6.x). We use the components in these libraries for designing the electronic hardware of the products we sell on our [website][2]. We've tested most of the footprints herein, and little by little we'll be adding whether they've been tested or not in the devices' description. Nonetheless, always, always test your board layouts by printing a 1:1 scale copy, and superimposing the physical components on it. 
If you find a mistake (wrong-sized footprints, mislabeled pins) [let us know][4] and receive a 10% discount on your next order! 

For clearly explained, step-by-step tutorials on using these libraries for designing your own electronic hardware please visit our [learning resources site][3].

Organization
---
We've organized the components into libraries according to their function to try to facilitate searching for each one of them.  Some organization choices are a matter of preference whereas others might have been done by mistake.  If you spot
something that could be done better please [let us know][4].  Currently, the components are organized as follows:

1. ''Ai_Boards'': typically shields for developments boards such as Blackjack and Arduino
2. ''Ai_Connectors'': USB, pin headers and sockets in different configurations (e.g., pad shapes, with or without silkscreen), SD cards, screw terminals, etc.
3. ''Ai_DiscreteSemis'': diodes, FETs, etc.
4. ''Ai_Electromechanical'': mechanical hardware (e.g., stand-offs), buttons, switches, etc. 
5. ''Ai_FrequencyControl'': crystals, resonators, etc.
6. ''Ai_IC'': digital and analog Integrated Circuits such as MCUs, shift registers, etc. (Excludes power ICs such as regulators, and RF ICs such as Wi-Fi and Bluetooth)
7. ''Ai_LED'': LEDs of all shapes and sizes.
8. ''Ai_Miscellany'': schematic frames, logos, and other non-electrical/-mechanical items.
9. ''Ai_Passives'': capacitors, inductors, resistors, fuses, beads, potentiometers, etc.
10. ''Ai_Power'': power ICs such as regulators, power symbols (e.g., GND, 5V, VIN, VBAT).
11. ''Ai_RF'': RF ICs including Wi-Fi and Bluetooth, RF connectors, antennas, etc.

Usage
---
To use these libraries please follow these simple steps:
1. Open the Eagle application, and select the `Control Panel` window
2. Using the top menu, select `Options` > `Directories`
3. The `Directories` window lets us specify the location of the libraries (as well as scripts, design rules, etc.).  In the first line (`Libraries`) we want to ''append'' the location of the contents of this repository (`Ai_Eagle_Libraries`). 

3.1. Option 1: assuming that the `Ai_Eagle_Libraries` repository was downloaded to the current user's home directory, simply change the text entry `$EAGLEDIR/lbr` to:

    $EAGLEDIR/lbr:$HOME/Ai_Eagle_Libraries (for OS X)

or,

    $EAGLEDIR\lbr;$HOME\Ai_Eagle_Libraries (for Windows)

Note: The `$HOME` part of the location specifies the home folder of the current user, thus these examples assume that the libraries were downloaded to this location.

3.2 Option 2: if we want the `Ai_Eagle_Libraries` residing with other custom libraries inside a `custom_libraries` directory we can choose the path:

    $EAGLEDIR/lbr:$HOME/custom_libraries (for OS X)

or,

    $EAGLEDIR\lbr;$HOME\custom_libraries (for Windows)

4. Click `OK` to save your changes. If the directory doesn't exist Eagle will ask to create one.  

If the folder already exists in your system and you get this prompt then select `No`, go back to step 2., select the option 'Choose' from the buttons on the `Directories` window, and select the location manually.  

If the folder did not exist, then select `Yes`. Afterward you'll need to move the downloaded `Ai_Eagle_Libraries` folder into the newly created location.

7. As of Eagle 6.5.0 you should be able at this point to see the `Ai_Eagle_Libraries` by selecting the `Control Panel` window, and expanding (clicking on `+`) the `Libraries` option.

8. To browse our components, expand the `Ai_Eagle_Libraries` option and subsequently expand any of the libraries therein (e.g., `Ai_Boards`, `Ai_Connectors`, etc.).

If you have any doubts about installation, usage, or troubleshooting the library and/or CadSoft's Eagle software check out our [PCB Design tutorials and guides][5].

License Information
---
All contents of this repository are licensed under a [Beerware License](http://en.wikipedia.org/wiki/Beerware).  If you find the libraries useful, and we happen to cross paths, you're encouraged to buy us a beer.

It'd be great to hear what you've built using these libraries, so [drop us a line][4] and we'll happily feature your latest creation on our blog!

![alt Beerware License](http://upload.wikimedia.org/wikipedia/commons/d/d5/BeerWare_Logo.svg)

[1]: http://www.cadsoftusa.com/ "CadSoft EAGLE PCB Design Sofware"
[2]: http://www.acrobotic.com/ "Acrobotic Homepage"
[3]: http://learn.acrobotic.com/ "Acrobotic Learning Resources"
[4]: http://acrobotic.com/contacts/ "Contact Acrobotic"
[5]: http://learn.acrobotic.com/eagle "Acrobotic Learning Resources"
