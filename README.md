<img width="540" height="828" alt="Drill, Baby, Drill Fallout Zine" src="https://github.com/user-attachments/assets/3fbc36ce-5c98-432a-b5b9-2e6e4ab624a9" /> 

<img width="655" height="678" alt="Screenshot 2026-05-25 201110" src="https://github.com/user-attachments/assets/1c5a517b-d5eb-4ad1-8d41-7e53f1e1b9c4" /> 

Trimetric view (with side panel removed)

<img width="615" height="735" alt="Screenshot 2026-05-25 201128" src="https://github.com/user-attachments/assets/27c5291a-2f86-4015-96e8-a23381fa8fcf" /> 

Profile view (with side panel removed)



# Drill-Baby-Drill
A custom-built 4-axis CNC mill designed from the ground up for precision metal machining, rigidity, and affordability.

## What is this?

This project is a fully custom CNC milling machine that we designed in CAD and are building ourselves for Hack Club. The machine uses aluminum extrusions, ball screws, linear rails, a spindle system, and a custom-designed 4th axis attachment to create a compact but capable CNC mill.

What makes this project unique is that we are trying to balance:
- Metal machining capability
- 4 axes
- Affordable components
- Compact size

Instead of buying an expensive commercial machine, we designed this mill ourselves, optimized the bill of materials to reduce costs, and made many CAD revisions to solve mechanical problems like frame flexing, rail alignment, collisions between axes, and spindle mounting.

Some notable features include:
- 3 linear degrees of freedom and 1 rotational degree of freedom
- Ball screw driven x-, y-, and z-axes for precision
- Steel linear rails for rigidity
- Fully custom CAD-designed aluminum
frame
- Expandable design for future automatic tool changing
- Enclosed electronics
- Compact footprint while maintaining large travel distances

Planned build volume:
- ~478.5 mm × 428.5 mm × 228.5 mm



## How to Use It

### CAD and Design

Most of the project development currently happens in CAD. We use CAD software to:
- Design the frame
- Position the axes
- Test motion and clearances
- Prevent collisions between parts
- Mount motors, rails, and ball screws
- Simulate the full machine assembly

The machine is designed around:
- 2020 aluminum extrusions
- HGR20 linear rails
- 1605 ball screws
- NEMA 23 stepper motors
- A 2.2 kW spindle with a VFD power supply

### Usage

Once fully assembled, the CNC mill will work like this:

1. Secure material onto the spoil board or rotary axis
2. Load a tool into the spindle
3. Generate toolpaths using CAM software
4. Send G-code to the CNC controller
5. The machine moves along the x-, y-, and z-axes using ball screws and linear rails
6. The spindle cuts the material while the frame maintains rigidity
7. Chips and debris are contained inside the enclosure

The optional 4th axis will allow rotational machining for more complex parts.



## Why We Made It

We made this project because we wanted to build a CNC mill that was:
- More affordable than commercial machines
- Capable of machining harder materials (including aluminum and possibly steel)
- Fully customizable
- A platform for experimentation and learning

A major motivation was learning mechanical design and engineering through a real project instead of only studying theory. We wanted to understand:
- CNC machine design
- Ball screws and linear rails
- Rigidity and structural engineering
- Manufacturing constraints
- Cost optimization

We also wanted to challenge ourselves by creating something significantly more advanced than a typical beginner CNC project. Many hobby CNC machines struggle with rigidity or precision, especially when machining metals, so a large focus of our work has been improving stiffness and reducing flex.

Another reason for building this machine was the opportunity to experiment with advanced ideas like:
- Automatic tool changing systems
- Coolant systems
- 4-axis machining
- Custom spindle mounting
- Chip protection systems
- Compact but rigid frame geometries

This project has involved a huge amount of iteration, problem solving, and redesigning, but that process has also been one of the most rewarding parts of building it.

## Tech Stack
### Hardware
- 2020 aluminum extrusions
- Steel HGR20 linear rails
- 1605 ball screws
- NEMA 23 stepper motors
- VFD spindle system
- Custom 4th axis chuck system
### Software
- Onshape CAD software
- Kiri:Moto CAM software
- gSender controller software
- grblHAL firmware



## Wiring Diagram
<img width="1543" height="1374" alt="CNC Wiring diagram (2)" src="https://github.com/user-attachments/assets/8a8e6997-1857-478c-b739-7a1e23534ef4" />



# Aluminum Extrusion Cut List

| Length (mm) | Quantity |
|------------|----------|
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



# Build Instructions

## 1. Preparing the Aluminum Extrusions

Cut all aluminum extrusions according to the cut list above.

After cutting:
- Deburr all edges
- Ensure cuts are square
- Clean chips from the internal channels

Using an M6 tap, thread the ends of every extrusion piece to a depth of approximately 20 mm. These threaded holes will be used to fasten adjoining frame members together.



## 2. Frame Assembly

Assemble the machine frame according to the CAD model.

To connect extrusions:
1. Slide M6 screws into the T-slots of the aluminum extrusion
2. Align the adjoining extrusion
3. Fasten the screws into the tapped holes on the end of the adjacent extrusion
4. Square and tighten the frame gradually to maintain alignment

During assembly:
- Avoid fully tightening components until the surrounding structure is aligned
- Check that all mounting surfaces remain parallel



## 3. Installing Linear Rails and Ball Screws

Mount the HGR20 linear rails onto the frame using M5 screws and M5 T-nuts.

When installing the rails:
- Tighten screws gradually in alternating patterns
- Verify rail parallelism before fully tightening
- Ensure smooth carriage movement across the full travel distance

Install the 1605 ball screws and bearing supports onto each axis.

After installation:
- Verify that the ball screws rotate freely
- Check for binding or misalignment
- Ensure couplers are centered between the motor shafts and ball screws



## 4. Mounting the Spindle and Work Surface

Install the spindle mount onto the Z-axis assembly and secure the 2.2 kW spindle in place.

Attach the spoilboard and MDF side panels using M5 screws and T-nuts.

Verify:
- Spindle clearance throughout the full machine travel
- No collisions between axes
- Proper alignment between the spindle and spoilboard



## 5. Electronics and Wiring

Mount the following components inside the electronics enclosure:
- Scylla v1 CNC controller
- VFD
- DC power supply

Wire all components according to the wiring diagram.

Important wiring considerations:
- Leave sufficient slack in all motor and limit switch wiring to accommodate X-, Y-, and Z-axis movement
- Secure cables to prevent interference with moving components
- Separate signal and power wiring where possible to reduce electrical noise
- Verify all grounding connections before powering the system



## 6. Calibration and Testing

After assembly:
1. Manually move each axis to verify smooth motion
2. Power on the electronics
3. Test motor direction and limit switches
4. Configure grblHAL settings
5. Calibrate steps/mm for each axis
6. Tram the spindle relative to the spoilboard
7. Perform low-speed test cuts before full operation

Recommended first tests:
- Foam
- MDF
- Acrylic
- Aluminum at conservative feed rates



# Safety Notes

- Always wear eye protection during operation
- Ensure the spindle is properly grounded
- Never leave the machine unattended while running
- Verify emergency stop functionality before use
- Contain chips and debris using the enclosure system
