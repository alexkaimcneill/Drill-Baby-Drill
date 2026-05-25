<img width="540" height="828" alt="Drill, Baby, Drill Fallout Zine" src="https://github.com/user-attachments/assets/3fbc36ce-5c98-432a-b5b9-2e6e4ab624a9" />


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

<img width="760" height="460" alt="Screenshot 2026-05-25 185421" src="https://github.com/user-attachments/assets/648e33d9-181c-427e-8c3e-fffc24cdb68e" /> 

y-axis ballscrew

<img width="350" height="684" alt="Screenshot 2026-05-25 185559" src="https://github.com/user-attachments/assets/4231a641-97a6-4863-a811-e10a8feef479" /> 

x-axis

<img width="172" height="649" alt="Screenshot 2026-05-25 185638" src="https://github.com/user-attachments/assets/8159f71b-2d3c-4f2f-95cb-00d9375c1558" /> 

z-axis



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
