# E2B_compass
CAD files for E2B compass model

This repository contains OpenSCAD model files for parts to build a replica model of an E2B standby compass.
Parts are numbered for easy reference.
STL files for each part are also included for immediate printing. No supports are required.
This collection is my MkIII design. MkI and MkII were for development.

The compass can be driven using the popular 28BYJ-48 stepper motor and electronics. See below for a list of
parts required to do this.

## How to assemble the model
First, print all the parts and tidy them up as usual. If you are going to paint the model then any colour is
fine, but dark colours are better. The actual E2B is currently available in black and grey. For convenience the
compass card (08) should be printed in black. The buck (09) is optional and is used as a vacuum-forming mould
so can be any colour as it is not itself used in the model.

### Postprocessing steps
#### 01 hex drive
The hex drive is the mechanical joint between the stepper motor and the compass card drive shaft. A hexagonal drive
shaft can be made by cutting the long part off a 3mm hex key. Ensure the end of the key is a snug fit in the
recess at the bottom of the part and won't fall out. Also ensure that the bottom face of the part is flat and smooth.
If you want to use a round shaft then drill out the hex-shaped hole to the size of the shaft (something like
3mm or 1/8" is recommended). Then tap the small hole at the side to accept an M3 grub screw so that the
drive shaft does not fall out.

The upper flat face is for an optical sensor (which detects the position of the stepper motor and drive
shaft in a driven model). Glue a circle of paper half black and half white onto this surface so that the
can reliably detect the position. Alternatively, if the part is white then stick a piece of black insulation
tape onto that face. If the part is black, stick a piece of white insulation tape or paper onto that face.

#### 02 plate
This is the plate that attaches the compass to the bulkhead. At the front edge are five small indentations.
These can be painted white for authentic adjustment marks if required. It may be necessary to drill the hole
in the top to allow the drive shaft to pass through and rotate freely.
There is a small circle on the top face of the model to indicate where there is a spigot on the original.
The spigot is not present in this model, and there is no file for it.

#### 03 body
The body of the compass is printed as a shell. Again, it may be necessary to drill the holes
in the top and bottom to allow the drive shaft to pass through and rotate freely. It may also be necessary
to cut or file any drooping filament inside the top edge of the aperture.

#### 04 lamp holder
The lamp holder has a round hole to accept an LED to light up the compass card in the same position as the
bulb on the original compass. The hole should be 5mm in diameter, and the LED should fit snugly. There is
a step around the hole of 6mm diameter to hold the flange of the LED
and stop it going too far into the hole. Next to the hole is a conduit hole which allows a thin cable
to be passed through and out of an exit hole on the bottom of the part. Next to this exit hole are two alignment holes.
These represent the electrical connections for the lamp on the original compass. Ensure these holes are clear
with a diameter of around 1.75mm to accept short pieces of 3D printing filament to act as alignment pins.
On the top of the lamp holder is a 3mm hole which should be cleared to allow the drive shaft to fit and rotate freely.
This hole is not deep and does not go all the way through the lamp holder!

#### 05 knob
On the original compass the knob was used to release the lampholder to change or service the bulb. This part
should be a press-fit into the large hole on the bottom of the lamp holder (04) and glued in place after
soldering wires to the LED and testing it.

#### 06 back plate
The back plate is modelled as a single part in OpenSCAD, but cut into two pieces for printing. Both pieces are
present in the STL file, ready to print. There are four alignment holes on the back of each of the two
parts. Again, these should be cleaned out to approximately 1.75mm so that short pieces of filament can be used to
align the two parts for gluing together.
At the bottom of the back plate is a protruding piece that represents the clamp on the original compass.
The hole through the clamp should be cleaned out to diameter 3mm for an M3x25 slotted cheese head screw and
nut to be fitted. The screw has no function in the model other than to give it a more authentic look.
The back plate is intended to be a snap fit in the back of the body (03). You can test-fit it and press it out
again afterwards.

#### 07 lamp lead
The lamp lead is modelled on the original lamp power connector. The original connector has a rubber 'Y' part
moulded onto the end of the lead. At the two tips of the Y are the electrical connectors that connect to the lamp holder
as mentioned above. The two sides of the Y are pressed together to allow them to connect to the pins, then
when they are released the rubber keeps pressure on the contacts to hold them in place. The model represents
the connector in the compressed position and has a small conduit through the centre for the LED wire to pass
through.
Remove the thin part on the underside of the model which acts as a support for the tube during printing, and
make sure the two holes at the ends of the Y are clear enough to accept pieces of filament for alignment.
Align the part with the lamp holder (04) and glue the two alignment pins to hold the parts together.
After feeding the LED cable through the part add a short piece of heatshrink tubing to support the cable in
the part.

#### 08 compass card
The compass card should be printed in black, or painted black. The hole down the centre is hexagonal to accept
the hexagonal drive shaft from part 01 above. Ensure the drive shaft is a snug fit in the hole. If you are using
a round shaft then drill out the centre to the appropriate diameter and install a grub screw in the small hole
on the side of the part.
Cut out and glue the compass card decal onto the compass card support. It should fit accurately. It is not
necessary to align the compass card decal with the shaft or optical mark on the hex drive (01). This will be
compensated for in software.

#### 09 buck
The final part is the buck. There is no separate OpenSCAD file for this part. Instead it is generated by changing
an option in the body file (03). The buck is used in conjunction with a small vacuum table and some PETG plastic
to mould a clear window that fits into the aperture and completes the look of the compass. The surface of the buck
has a thin ridge that will be visible in the window. This is the lubber line of the compass and should be painted
with a thin line of white paint on the inside of the window.
It will be necessary to fill and sand the buck to smooth out the 3D printed lines that would otherwise be visible
in the PETG when it is softened to mould it. Ensure that the small semicircle moulded from the bottom of the buck is
removed. This will allow enough clearance for the compass card to sit flat at the bottom of the inside of the body.

### Final assembly
Once the parts are prepared, install the LED into the lamp holder (04) and feed the LED power cable through the
conduit and solder it to the LED. Test the LED then glue the knob (05) onto the bottom of the lamp holder. Feed
the LED cable through the lamp lead (07). Insert pieces of filament into the two holes in the lamp lead, attach
it to the lamp holder and glue it in place. Add heatshrink to the point where the cable exits the lamp lead part,
although this can be done later.

Hold the plate (02), body (03) and assembled lamp holder (04) together and test fit. Use the drive shaft to ensure
that the holes through all of these parts are in alignment and then glue them together.

Glue the front window in place if you chose to make it.

Put the compass card inside the body and push the drive shaft through it from above. It should enter the hole
in the bottom of the body, and can extend into the hole in the lamp holder if necessary. Tighten the grub screw if
you are using one. Press the back plate (06) into place. It is not necessary to glue the back plate, and it can
be removed later if necessary.

### Connecting the motor
Instructions for motorising the compass and attaching it to a data feed from a flight simulator will be added later.
