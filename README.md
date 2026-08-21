# Hybrid Earthquake Vibration Control for Buildings

Design and experimental validation of a **hybrid active–passive vibration control system** for a 3-storey building model, developed as a Design Lab (ME-306) project.

## Project Overview

A ~3 ft acrylic and MDF scale model was designed to study structural vibrations under simulated seismic excitation. The system combines **spring-based passive isolation** with **PID-controlled active damping** to reduce structural vibrations.

## Key Features

- 3-storey acrylic building model (~0.9 m, ~1.2 kg)
- Four spring-based base isolators
- ANSYS modal and harmonic-response analysis
- Arduino Mega-based PID controller
- MPU6050 accelerometer for real-time vibration feedback
- High-torque servo for active counter-torque
- Hybrid passive + active vibration control

## System Architecture

**Seismic Excitation → Spring Isolators → Building → MPU6050 → Arduino Mega (PID) → Servo → Counter-torque**

Passive isolation attenuates the primary ground excitation, while the active control system suppresses residual vibrations through real-time feedback.

## Analysis

Modal analysis was performed in **ANSYS 2025 R2**.

| Mode | Frequency |
|------|-----------|
| 1st lateral bending | 4.846 Hz |
| 2nd lateral bending | 13.506 Hz |
| Torsional | 18.417 Hz |
| Higher lateral | 18.88 Hz |

The first two modes were identified as the critical design frequencies for vibration control.

Harmonic response analysis was also performed to study the structural response under excitation.

## Control System

The active damping system uses:

- **Arduino Mega 2560** – PID control and servo actuation
- **MPU6050** – 6-DOF accelerometer/gyroscope for vibration feedback
- **High-torque servo** – generates counter-torque to suppress vibration

The PID controller uses acceleration error as feedback to determine the required actuator response.

## Experimental Setup

The physical system consists of:

- 16 acrylic columns
- 6 MDF floor slabs
- MDF base plate
- 4 coil springs
- Arduino Mega
- MPU6050
- High-torque servo
- Separate power supply for the servo

## Tools Used

- ANSYS 2025 R2
- Arduino
- MPU6050
- PID Control

<img width="1547" height="791" alt="Modes on Ansys" src="https://github.com/user-attachments/assets/ece05a0b-c17f-42bb-8d8b-7f77cfc3fdac" />




## Project Status

**Completed**
