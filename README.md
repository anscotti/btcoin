Allow me to introduce to you the BantamCoin (TM): spend one to get back your broken endmill!
The CNC mill I have access tois a pretty standard German made 3020 from my makers club: nothing special, but reliable with a decent precision.

I designed the coin in Fusion360 and, as you could guess, I was looking for a challenge: curved surfaces, inset features and parts relying on machining operations to become visible; things I had never tried before. 
To machine all that on a 3 axis cnc mill I had to split the work into two setups: one for the top side and one for the bottom side and take into account how the part would remain fixed until the very last second.

![3D Rendering](../master/coin.jpg?raw=true)

Luckily Fusion360 helped me a lot in the process, but not as much as to prevent me to perpetrate some mistakes and break some bits: unluckily the coin wasn't available yet, so I couldn't spend it to regain the broken parts.

As for the material, I did notice a few months ago a piece of 8mm aluminium onto which some unknown entity, probably from a parallel universe, had used a blue permanent marker to write down some misterious digits: "6061".

My initial intention was to use a radial finish on the curved surfaces, but I discovered very late in the machining process that wasn't a viable process: the coin was freed up from the stock a bit too earlier due to the extra clearance required to mill the sides with a 1/8" ball endmill.

Lesson learned, try again.

## The miling process

The two setups (top and bottom) differ each other on Z and X axis being flipped: this allows for the stock material to be rotated along the Y axis only, but you need to have a squared stock and a precise measure of its length along the X axis.

#### Let's clear it up
I started with a 3D adaptive clearing strategy executed with a flat 1/8" by 8mm 2 flutes carbide endmill. The process was estimated to last 20mins 20secs at 16kRPM 330mm/min ramping into the stock at 220mm/min and leaving 0.5mm stock for finer surfacing.

> Applies on both sides

![3D Adaptive Clearing](../master/adaptive.png?raw=true)

#### Refine the sides
The inset features are challenging as they require a smaller and more fragile 2.0mm 2 flutes carbide endmill (I broke one at my first try) so I had to split this task in two steps:

 * remove more material with the 1/8" by 8mm endmill using a negative "axial stock to leave" parameter for a 3D contour strategy, expected to last 3mins at 16kRPM 330mm/min with a 0.2mm stepover
 * refine the result with the 2.0mm by 12mm 2 flutes carbide endmill at 16kRPM 200mm/min which now have little work to do, but stil run with 0.2mm stepover for 6mins

> Applies on both sides

![3D Contour - Rough Pass](../master/contour-rough.png?raw=true)
![3D Contour - Fine Pass](../master/contour-fine.png?raw=true)

#### A shiny surface

The concave coin surface is made by two separate spirally actions, both having a 0.2mm stepover to maximize surface quality:
 * the inner part uses a 1/8" ball 2 flutes carbide endmill and consumes 8.5 mins at 16kRPM at 350mm/min with a "stock to leave" setting of 0.05mm (both radial and axial)
 * the outer part is made by 2.5mm ball 2 flutes carbide endmill running for 7 mins at 16kRPM at 250mm/min, again with  a "stock to leave" setting of 0.05mm (both radial and axial)

> Applies on both sides

![3D Radial - Inner Pass](../master/spiral-inner.png?raw=true)
![3D Radial - Outer Pass](../master/spiral-outer.png?raw=true)

#### Engraveyard

The BantamTools roster is only 0.05mm in depth, but the different milling strategy reflets the light in a very different way, allowing the roster to appear clearly when the light is cast at an angle. The operation is estimated at 2.5 mins at 12kRPM 600mm/min using a 0.2mm 20° pyramidal shaped endmill, which I configured in Fusion360 as a chamfer endmill to be used with the scallop 3D strategy with a 0.33mm stepover.

> Top side only

![3D Scallop](../master/top-scallop.png?raw=true)

#### Prepare to flip over

Before flipping over the stock a final contour pass is run with the 1/8" flat endmill ensuring the sides of the coin are shining and smooth, but leaving enough axial stock so that all other operations which will be run on the other side have enough material left: the idea is only the inset features will have no support material.

The operation is supposed to last only 1.5 mins at 16kRPM 330mm/min.

> Top side only

![3D Contour](../master/releave.png?raw=true)

#### The dark side of the coin

Turning the stock upside down and maintaing the necessary alignment was probably the trickiest part, but the side clamps helped, apart for a slight misalignement and the constant terror I did fail the alignment which accompanied me for the last 2 hours of milling...

#### Player one, get ready.

The "EXTRA LIFE" text is created with two separate operations, all using a 0.1mm 20° pyramidal carbide endmill with a 600mm/min feedrate and a 30mm/min plunge speed while spinning at 12kRPM:

 * a 3D parallel operation with a 0.1mm stepover, using the projected sketch for containement with an additional 0.15mm inward offset (to prevent marks on the border) but using a 0° orientation (so to have a nice surface effect) for 1 min 40 secs
 * a trace operation along the sketch I projected for 1 min 20 secs

![3D Parallel](../master/bottom-parallel.png?raw=true)
![2D Trace](../master/bottom-trace.png?raw=true)

> Bottom side only

#### Release

Finally I used a 3 flute 1/8" carbide flat endmill with a contour operation leaving a couple of tabs to keep the coin in place. 

> Bottom side only

![3D Contour](../master/contour.png?raw=true)
