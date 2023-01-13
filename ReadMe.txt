These are the files I used to create the RVL-129X, a Wii on a BVM card. It is based on Martin's card. This project is essentially me craming his circuit into the corner, and adding pads to 1: solder the controller ports to and 2: bolt the Wii on. Consult his github for more info on the capabilities of the card portion of this project, as well as the software to program the Arduino.

It was a quick and dirty project not originally intended for public release. I am releaseing the files as is due to popular demand. It is cluttered, unoptimized, and made for my specific circumstances and my available parts. Sorry in advance.

Follow the Definitive Wii trimming gudie for information on how to trim and run the Wii. Standard trim. Run YPbPr and audio through shielded wire to the marked pads. SH is ground for shielding. Connect Controller lines to controller pads. 4 Layer Wii highly recommended. Leave the 1.8v LDO on the Wii. Do not connect mode pin to 3.3v if your PVMs are 15khz only, as this enables 31khz.

The 129x card cannot pass audio through the slot, so audio comes out a 3.5mm jack and into the RCA jacks on the back. 

For voltage regulators, I purchased and bolted on an RVL-PSU. It contains all the voltage regulator rails the Wii needs. It is open source. You can assemble one yourself, use the open source design to integrate it onto this PCB, buy an RVL-PSU from CrazyGadget on the Bitbuilt forums, or design your own regulators if you are a pro. Do not use generic chinese voltage regulator boards, their power is not clean and will cause issues.

I included overkill voltage protection for every voltage rail of every controller port. This is because I plan to take it to Melee tournaments. The competitive Melee conroller modding scene has a huge problem with design and quality control of aftermarket and modded controllers. Many systems at tournaments have destroyed components caused by controllers overdrawing the voltage rails. These components are overkill, expensive, and tedious to solder. If these circumstances are not relevant to you, you can omit these components placed by the controller ports, and instead run 3.3v and 5v directly to the 3.3v and 5v pins of the controller ports with wires. 

Near the solder pads for the gamecube controller data wires are some diodes and filters. These are harvested from the lines connected to the data lines on the Wii motherboard. Diodes are for extra ESD protection. Filters can probably be jumpered over, but probably not best practice.

Resistors R2, R3, R4 and R5, along with R14, R15, R16 and R17 are not populated on this board. Csync pad is not used.

For screws I used the silver screws inside the wii, used mostly on the EMI shield.

For the fan and heatsink my usual setup: 35mm x 35mm x 7mm fan with 35mm x 35mm x 7mm heatsink, along with a 35x70mm copper plate. This setup has become the go-to in the portablizing community, and is used on many portables like the G-Wii. Use thermal paste between heatsink and copper plate. Use thermal pad between CPU/GPU and copper plate.

I didnt really plan where to put the USB port. I used a USB to micro SD card adapter, and mounted it to a GCC controller port with double sided foam adhesive tape. 

Theres an LDO (U5) that I didn't include on BOM because the replacement I purchased had a different pinout. I had to bodge it, but I added a jumper in case your LDO has that pinout. Check his github for specs on that part.

Included are 2 STLs that need to be printed. One is for mounting the Wii and the cooling system to the board. The other is the back plate. The back plate has 2 versions. V2 is the one I used. The extrusions for the screws are a little flimsy, so i made V3 to strengthen them. It should work and be stronger, but I never tested it so I included both. All 3d printed parts are mounted with silver scews from the Wii.

Order PCB with 1.6mm thickness. Its a 2 layer board, nothing special.

If you use this project, please credit me. Would love to see what people make with this. If you plan to monetize, please contact me.  



Troubleshooting tips I wish I knew:

Arduino must be programmed using the header. It WILL NOT WORK if programmed through the USB port on the arduino. 

Make sure U2 is being powered by U5 regulator. Different LDOs in that package have different pinouts. 

You can troubleshoot the signal chain by taking the Luma signal and skipping U2 and U1



