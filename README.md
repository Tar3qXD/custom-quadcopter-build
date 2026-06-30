# Custom Autonomous/Programmable Quadcopter Build

## Project Overview

This project is a custom quadcopter build focused on gaining practical experience in embedded systems, electronics, programming, debugging, teamwork, and engineering documentation.

The goal is to build a drone from individual hardware components, assemble the system, configure the flight controller, and eventually add programmable features. This project is being developed as a portfolio project to demonstrate hands-on electrical and computer engineering skills.

## Version 1 Goal

The first version of the project will focus on building a basic stable quadcopter that can:

* Power on safely
* Arm and disarm properly
* Connect to a flight controller configuration tool
* Fly manually in a controlled environment
* Be tuned and tested safely

Advanced features such as GPS navigation, autonomous flight, computer vision, or obstacle avoidance may be explored later after the basic drone is working.

## Skills Demonstrated

* Embedded systems
* Electronics and wiring
* Flight controller setup
* Sensor and control system understanding
* C/C++ or Python programming
* Debugging and troubleshooting
* Budget planning
* Engineering documentation
* Team collaboration

## Current Status

The project is currently in the planning and research stage. The main focus is to choose a realistic build path, define the first working version, and create a budget before purchasing hardware.

## Planned Milestones

1. Define project scope and Version 1 requirements
2. Compare possible build paths
3. Create a budget and parts list
4. Purchase hardware
5. Assemble frame, motors, ESCs, and flight controller
6. Configure the flight controller
7. Perform safety checks
8. Complete first test flight
9. Document problems, fixes, and lessons learned
10. Explore programmable or autonomous features


## Build Path Decision

We are currently comparing two possible build paths:

### Option 1: Betaflight-style FPV quadcopter
This path is common for manual flight and racing/freestyle drones. It may be cheaper and easier to get flying quickly.

### Option 2: Pixhawk/ArduPilot-style drone
This path is better for GPS, autonomous flight, and advanced programmable features, but may be more expensive and more complex.

We will compare both options based on cost, difficulty, documentation, software flexibility, and portfolio value before choosing a final direction.

## Software Development Approach

The software side of this project will be developed using an AI-assisted but student-led approach. The goal is not to let AI complete the project for us, but to use it as a learning and debugging tool while we make the engineering decisions ourselves.

For the first version of the drone, we do not plan to write the entire flight control system from scratch. A full flight control system involves sensor processing, stabilization, PID control, motor mixing, arming logic, safety checks, and communication with the receiver. Writing all of this from zero would be unrealistic and unsafe for the first stage of the project.

Instead, Version 1 will focus on using existing flight controller software and configuration tools to safely build, configure, test, and fly the drone. This will allow us to gain hands-on experience with the hardware, wiring, firmware setup, calibration, debugging, and tuning process.

C++ will still be an important part of the project. We plan to use C++ for learning core embedded systems concepts, writing small test programs, creating simulations, understanding control logic, and possibly developing custom features later in the project.

AI may be used to explain concepts, help debug code, review documentation, and suggest possible approaches. However, all final decisions, testing, implementation, and documentation will be done and understood by us.


## Build Path Research Notes

### Betaflight-style build
Pros:
- Its flight performance is great for racing and doing flips (freestyle). Software translates hand movements to the drone without any delay.
- Gives knowledge and experience on repairability without relying on manufacturer to repair it.
- very popular, thus, finding tutorials and help on Betaflight Website or FPV forums is simple.

Cons:
- Must learn soldering and understand electronics, tuning the software can be lengthy.
- has no safety net, thus letting go of the controller will make the drone fall, it lacks automation hover in place or fly itself back, unless a GPS modification is added
- Installing wrong parts together can make the drone short-circuit, overheat, or crash

### ArduPilot/Pixhawk-style build
Pros:
- this system excel at complex waypoint missions, mapping grids, auto-takeoffs, and auto-landings.
- many Pixhawk boards offer redundant (bakcup) compasses, barometers, and IMUs (sensors that measure orientation and movement) to prevent crashes if a component fails.
- can be programmed to trigger specific action (such as "Return to Launch" or "Parachute deploy") if connection is lost or battery level drop too low.

Cons:
- High-quality Pixhawk boards and accessories (like specialized GPS and telemetry modules) are expensive compared to standard, off-the-shelf drone parts.
- configuring the setup requires specialized software like Mission Planner or QGroundControl. Means to calibrate sensors and set up hundreds of parameters manually.
- Unike "plug-and-play" drones, building a Pixhawk drone requires many manual connections and wiring. Thus, this adds weight and complexity to the build.

### Current leaning
We are currently leaning toward: ArduPilot/Pixhawk

Reason:
Pixhawk/ArduPilot seems like the better learning path, but we should only choose it if the cost, difficulty, and timeline stay realistic.
