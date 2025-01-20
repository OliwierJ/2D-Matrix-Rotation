# 2D Matrix Rotation

This repository contains a program written in **m68k assembly**, created using the EASy68k development environment and tested with the EASy68k simulator. The program demonstrates 2D matrix rotation by plotting and rotating a square on the screen.

## Overview

The program:
- Plots points to draw a square on the screen using m68k's graphics mode.
- Simulates a Cartesian plane for positioning points on the screen.
- Performs square rotation using a **2D rotation matrix**.

## Key Features

- **Pre-computed Trigonometric Values:**
  - All _sine_ and _cosine_ values required for rotation are pre-computed and stored in memory as a table of long values.

- **Fixed-Point Arithmetic:**
  - Since m68k lacks built-in decimal number support, _sine_ and _cosine_ values are scaled by \(10^4\) to emulate fixed-point arithmetic.
  - The scaling is reversed during the final position calculation for each screen coordinate.

## Limitations

Due to the scaling and lack of native decimal support, the program may encounter minor precision errors in the rotation calculations. These errors are negligible for most purposes but may become noticeable with extensive rotations.

## Requirements

- **EASy68k Simulator:**
  - To run and test the program, you need the EASy68k environment.

## Usage

1. Open the program in the EASy68k editor.
2. Run the simulation using the EASy68k simulator.
3. Observe the square's rotation on the simulated screen.

## Additional Notes

This project serves as an educational example of implementing 2D matrix rotation in assembly language, demonstrating both the challenges and techniques involved in low-level graphical computations.
