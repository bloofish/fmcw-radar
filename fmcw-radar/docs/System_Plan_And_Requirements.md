# System Plan and Requirements Document

## Purpose and Scope
The purpose of this system is to build a working frequency-modulated continuous-wave radar that produces a two-dimensional, top-down map of its surroundings. It will handle signal generation, reception, processing, rotation, and display to show object range and position.

## System Overview
The system operates as a frequency-modulated continuous-wave radar. It transmits a linearly swept radio signal and receives reflections from surrounding objects. The transmitted and received signals are mixed to produce a beat frequency that corresponds to target distance. Major components include a voltage-controlled oscillator for signal generation, antennas for transmission and reception, a mixer and amplifier for signal conditioning, an analog-to-digital converter for sampling, an FPGA for processing and control, a motorized platform for rotation, and a computer interface for visualization.

## Functional Subsystems
- **Signal Generation** – Produces the swept-frequency transmit signal using a voltage-controlled oscillator driven by a digital control source.  
- **Transmission and Reception** – Uses directional antennas to radiate the signal and collect reflections from objects in the environment.  
- **Receiver Front-End** – Amplifies the received signal and mixes it with a reference copy of the transmitted signal to produce a lower-frequency beat signal.  
- **Data Conversion** – Converts the analog beat signal into digital samples for processing.  
- **Processing Core** – Implements timing control, signal processing, and range extraction using an FPGA.  
- **Rotation and Positioning** – Mechanically rotates the radar head and records angular position to build a two-dimensional map.  
- **Visualization and Control Software** – Runs on a computer to display radar data in real time and provide system control.  
- **Power Supply and Housing** – Provides stable power and mechanical support for all subsystems.  

## System Requirements
- **Operating Frequency:** 2.4 GHz ISM band for legal, low-power operation.  
- **Range:** Detect targets within 10 m.  
- **Range Resolution:** Better than 0.5 m based on sweep bandwidth.  
- **Angular Coverage:** 0–360° through continuous rotation.  
- **Angular Resolution:** ≈ 5° per step for balanced detail and speed.  
- **Scan Rate:** Less than 2 seconds per scan.  
- **Transmit Power:** ≤ 100 mW to meet ISM limits.  
- **Power Consumption:** < 15 W overall.  
- **Supply Voltage:** 12 V DC regulated.  
- **Interface:** USB or serial link to host PC.  

## Constraints
- Operates in the 2.4 GHz ISM band with transmit power ≤ 100 mW.  
- Uses off-the-shelf FPGA and low-cost RF components.  
- 12 V DC supply, total power < 15 W.  
- USB or serial connection to PC.  

## Verification Plan
- **Range (≥ 10 m):** Test using a target placed at 2, 5, and 10 m. Confirm clear detection with signal-to-noise ratio above 6 dB at each.  
- **Range Resolution (≤ 0.5 m):** Place two targets separated by 0.5 m at a fixed distance of around 5 m. Verify two distinct range peaks in the processed data.  
- **Transmit Power (≤ 100 mW):** Measure output power. Confirm that effective radiated power does not exceed 100 mW.  
- **Power Consumption (≤ 15 W):** Monitor total current draw at 12 V during operation. Verify that average consumption remains below 15 W with all subsystems active.  
- **Supply Voltage (12 V DC):** Power system from a 12 V regulated source and monitor voltage stability during normal operation.  

## Project Management and Version Control
GitHub  

## References
- [https://en.wikipedia.org/wiki/Frequency-modulated_continuous-wave_radar](https://en.wikipedia.org/wiki/Frequency-modulated_continuous-wave_radar) – General overview of FMCW radar principles, operation, and applications.  
- [https://www.ti.com/lit/an/swra553a/swra553a.pdf](https://www.ti.com/lit/an/swra553a/swra553a.pdf) – Texas Instruments application note explaining FMCW radar fundamentals and signal processing concepts.  
- [https://www.ecfr.gov/current/title-47/part-15](https://www.ecfr.gov/current/title-47/part-15) – U.S. FCC regulations governing low-power unlicensed transmitters in ISM frequency bands. Similar to the UK.  
