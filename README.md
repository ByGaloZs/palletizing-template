# Palletizing Template (Doosan DRL Script)

This repository contains a generic palletizing script written in **DRL (Doosan Robot Language)**, designed to run **directly on the Doosan robot controller**. It serves as a reusable foundation for basic palletizing operations in industrial environments.

## Current Functionality

- Setup of joint and linear motion speeds and accelerations.
- Digital output control for vacuum grippers.
- Predefined positions for pick, place, and home.
- Safe approach and retraction logic for all movements.
- Parameterization of box and pallet height.

> Note: This script is designed to run exclusively on the robot controller and is not integrated with external systems or simulators.

## Future Plans

This repository will serve as the base for a future restructured version, with the following goals:

- Migrate the logic to an **object-oriented Python project**.
- Enable integration with tools such as **ROS**.
- Design a scalable architecture for flexible and reconfigurable palletizing systems.


## Requirements

- Doosan robot controller
- Basic knowledge of DRL programming

## Manual Setup

Before running the script, you must manually teach all positions of the first and second pallet layers using the robot teach pendant. These positions are critical for the script to calculate the complete palletizing pattern.

Specifically:

- **First layer (Pattern A)**: Teach all 9 positions of the first pallet layer.
- **Second layer (Pattern B)**: Teach all 9 positions of the second pallet layer.

These two layers define the box spacing, rotation, and orientation rules for alternating patterns. The script uses them to generate all remaining layers dynamically.
Make sure to teach these positions using the correct user coordinate frame (e.g., user_coordinates_101) as referenced in the script.

## Author

Developed by [Mario Padilla](https://github.com/ByGaloZs), Mechatronics Engineer with professional experience in industrial robotics and automation.

---

This project is under active development and will be improved in future iterations.
