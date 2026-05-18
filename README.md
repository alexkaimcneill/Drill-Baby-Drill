# Drill-Baby-Drill
A custom-built 4-axis CNC mill designed from the ground up for precision metal machining, rigidity, and affordability.

## What is this?

This project is a fully custom CNC milling machine that we designed in CAD and are building ourselves for Hack Club. The machine uses aluminum extrusions, ball screws, linear rails, a spindle system, and a custom-designed 4th axis attachment to create a compact but capable CNC mill.

What makes this project unique is that we are trying to balance:
- High rigidity
- Metal machining capability
- 4-axis functionality
- Affordable components
- Compact size

Instead of buying an expensive commercial machine, we designed nearly every part ourselves, optimized the bill of materials to reduce costs, and iterated through many CAD revisions to solve mechanical problems like frame flexing, rail alignment, collisions between axes, and spindle mounting.

Some notable features include:
- Custom-designed 4-axis rotary system
- Ball screw driven x-, y-, and z-axes for precision
- Steel linear rails for improved rigidity
- Fully custom CAD-designed frame
- Expandable design for future automatic tool changing
- Enclosed electronics
- Compact footprint while maintaining large travel distances

Current planned build volume:
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

### Planned Machine Workflow

Once fully assembled, the CNC mill will work like this:

1. Secure material onto the spoil board or rotary axis
2. Load a tool into the spindle
3. Generate toolpaths using CAM software
4. Send G-code to the CNC controller
5. The machine moves along the x-, y-, and z-axes using ball screws and linear rails
6. The spindle cuts the material while the frame maintains rigidity
7. Chips and debris are contained inside the enclosure

The optional 4th axis will allow rotational machining for more complex parts.

### Design Challenges We Solved

During development, we encountered many engineering problems, including:
- Axis collisions between the spindle frame and ball screws
- Flexing in aluminum extrusion supports
- Rail alignment inconsistencies
- Limited z-axis travel for the 4th axis
- Mounting solutions for the spindle and motors
- Wire management across moving axes
- Protecting rails and screws from machining debris
- Material selection for machine panels and spoil boards

To solve these problems, we:
- Switched to stronger steel linear rails
- Reinforced the frame with additional extrusions
- Reworked axis geometry multiple times
- Reduced unsupported spans to improve rigidity
- Redesigned spindle mounting orientation
- Optimized the BOM to reduce costs
- Experimented with safer enclosure materials like PVC instead of MDF in some areas



## Why We Made It

We made this project because we wanted to build a CNC mill that was:
- More affordable than commercial machines
- Capable of machining harder materials (including aluminum and possibly steel)
- Fully customizable
- A platform for experimentation and learning

A major motivation was learning mechanical design and engineering through a real project instead of only studying theory. We wanted to understand:
- CNC machine design
- Motion systems
- Ball screws and linear rails
- Rigidity and structural engineering
- CAD workflows
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
- CAD modeling software
- Kiri:Moto CAM software
- gSender controller software
- grblHAL firmware
