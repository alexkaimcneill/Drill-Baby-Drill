![Drill, Baby, Drill Zine](https://github.com/alexkaimcneill/Drill-Baby-Drill/blob/main/Drill%2C%20Baby%2C%20Drill%20Fallout%20Zine.pdf)
****


<img width="655" height="678" alt="Screenshot 2026-05-25 201110" src="https://github.com/user-attachments/assets/1c5a517b-d5eb-4ad1-8d41-7e53f1e1b9c4" />

Trimetric view (side panel removed)

<img width="615" height="735" alt="Screenshot 2026-05-25 201128" src="https://github.com/user-attachments/assets/27c5291a-2f86-4015-96e8-a23381fa8fcf" />

Profile view (side panel removed)

# Drill-Baby-Drill

A 4-axis CNC mill we're designing and building from scratch for Hack Club, built to actually cut metal without costing what a commercial machine costs.

## What is this

This isn't a router that flexes the second you look at aluminum wrong. It's a real CNC mill: aluminum extrusion frame, ball screws, linear rails, a spindle system, and a 4th axis attachment we designed ourselves. We modeled the whole thing in CAD and we're building it piece by piece.

The hard part is doing four things at once: cutting metal, running 4 axes, keeping the BOM cheap, and keeping the footprint small. Machines that hit all four cost more than we had, so we designed our own. That meant reworking the BOM over and over to cut cost, and a long stack of CAD revisions to fix frame flex, rail alignment, axis collisions, and spindle mounting.

Specs:
- 3 linear axes + 1 rotational axis
- Ball screw driven X, Y, Z
- Steel linear rails for rigidity
- Fully custom aluminum frame, designed in CAD
- Room to add auto tool changing later
- Enclosed electronics
- Small footprint, long travel

Build volume: 478.5 mm × 428.5 mm × 228.5 mm

## How to use it

### CAD and design

Right now most of the real work happens in CAD, not the shop. We use it to:

- design the frame
- place the axes
- check motion and clearance
- catch collisions before we cut anything
- mount motors, rails, and screws
- run the full assembly as a simulation

Parts we designed around: 2020 aluminum extrusion, HGR20 linear rails, 1605 ball screws, NEMA 23 steppers, and a 2.2 kW spindle on a VFD.

### Running it

Once it's built, here's the loop:

1. clamp material to the spoilboard or the rotary axis
2. load a tool in the spindle
3. generate toolpaths in CAM
4. send G-code to the controller
5. the machine drives X, Y, and Z on ball screws and linear rails
6. the spindle cuts while the frame holds rigid
7. the enclosure keeps chips where they belong

The 4th axis adds rotational machining for parts a 3-axis mill can't touch.

## Why we built it

We wanted a CNC mill that's cheaper than a commercial one, can actually cut aluminum and maybe steel, and is ours to modify however we want.

The bigger reason: we wanted to learn mechanical design by building something real instead of just reading about it. That meant figuring out ball screws and linear rails, rigidity and structural design, what's actually manufacturable, and how to cut cost without cutting corners.

We also wanted to build something harder than the usual hobby CNC project. Most hobby machines flex too much or lose precision the moment you try to cut metal, so a lot of our time went into stiffening the frame and killing flex.

Along the way we're also experimenting with auto tool changing, coolant, 4-axis machining, custom spindle mounting, chip containment, and frames that are rigid without being huge.

It's been a lot of redesigns and a lot of problem solving, and that's also been the most fun part of the whole build.

## Tech stack

**Hardware**
- 2020 aluminum extrusion
- Steel HGR20 linear rails
- 1605 ball screws
- NEMA 23 steppers
- VFD spindle system
- Custom 4th axis chuck

**Software**
- Onshape (CAD)
- Kiri:Moto (CAM)
- gSender (controller)
- grblHAL (firmware)

## Wiring diagram

<img width="1543" height="1374" alt="CNC Wiring diagram" src="https://github.com/user-attachments/assets/8a8e6997-1857-478c-b739-7a1e23534ef4" />

## Aluminum extrusion cut list

| Length (mm) | Quantity |
|---|---|
| 80 | 8 |
| 115 | 1 |
| 125.5 | 2 |
| 147 | 4 |
| 152.5 | 4 |
| 155 | 4 |
| 160.75 | 4 |
| 190.25 | 2 |
| 267 | 2 |
| 350 | 4 |
| 381 | 2 |
| 486 | 6 |
| 523.5 | 2 |
| 570 | 3 |
| 573.5 | 2 |
| 590 | 1 |
| 670 | 6 |
| 700 | 8 |
| 702 | 4 |
| 900 | 4 |

## Build instructions

### 1. Cut the extrusions

Cut everything on the list above. Deburr every edge, make sure the cuts are square, and clean the chips out of the internal channels.

Tap the ends of every piece with an M6 tap, about 20 mm deep. That's what holds the frame together.

### 2. Frame assembly

Build the frame off the CAD model. To join two extrusions:

1. slide M6 screws into the T-slot
2. line up the next extrusion
3. thread the screws into the tapped holes on its end
4. square up the frame and tighten gradually as you go

Don't crank anything down fully until the surrounding structure is aligned. Check that mounting faces stay parallel as you tighten.

### 3. Linear rails and ball screws

Mount the HGR20 rails with M5 screws and T-nuts. Tighten in an alternating pattern and check parallelism before fully tightening. Carriages should move smooth across the whole travel, if they don't, something's off.

Install the 1605 ball screws and bearing supports on each axis. After they're in, spin them by hand, check for binding or misalignment, and make sure the couplers are centered between motor shaft and screw.

### 4. Spindle and work surface

Mount the spindle to the Z-axis and bolt in the 2.2 kW spindle. Attach the spoilboard and MDF side panels with M5 screws and T-nuts.

Check spindle clearance through the full travel, make sure nothing collides between axes, and confirm the spindle lines up with the spoilboard.

### 5. Electronics and wiring

Inside the enclosure: Scylla v1 controller, VFD, and DC power supply. Wire it per the diagram above.

A few things that actually matter here:

- leave slack in motor and limit switch wiring so it doesn't yank when X, Y, Z move
- secure cables so nothing snags on moving parts
- keep signal and power wiring apart where you can, it cuts noise
- check every ground before you power anything on

### 6. Calibration and testing

1. move each axis by hand, check it's smooth
2. power on the electronics
3. check motor direction and limit switches
4. configure grblHAL
5. calibrate steps/mm on each axis
6. tram the spindle to the spoilboard
7. run slow test cuts before anything at full speed

First cuts to try: foam, MDF, acrylic, then aluminum at conservative feeds.

## Safety

- wear eye protection, every time
- ground the spindle properly
- never leave it running unattended
- check the e-stop works before you use the machine
- keep the enclosure closed to contain chips

## Demonstration

[![Watch the video](https://img.youtube.com/vi/KmNqm5aDeno/maxresdefault.jpg)](https://youtu.be/KmNqm5aDeno)
