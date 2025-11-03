### Rotation & Positioning

Rotates the radar antennas to build the 2D map. A small microcontroller drives a stepper motor.

- **Motor:** Use a stepper for predictable and repeatable rotation.
- **Scan time:** Full 360° rotation completed in ≤ 2 seconds (slower modes allowed).
- **Motion:** Can rotate continuously or in small steps as long as spokes are consistent.
- **Angle reporting:** Micro sends a step count or simple angle reference to the FPGA each chirp.
- **Homing:** Basic zero-point reference to define the start position.
- **Mechanical:** TX/RX antennas rotate together and stay aligned.
- **Power:** Runs from the system 12 V with local regulation for the motor driver.
- **Noise:** Keep motor wiring away from RF paths to avoid interference.
