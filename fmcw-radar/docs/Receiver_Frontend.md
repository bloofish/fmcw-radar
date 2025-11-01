### Receiver Front-End

Converts weak 2.4 GHz echoes into a clean low-frequency beat signal for the ADC.
LNA → mixer → IF filtering/gain

- **Input:** 50 Ω RF from the RX antenna within the 2.400–2.4835 GHz band.  
- **Gain/Noise:** Enough low-noise gain to detect targets at 10 m while avoiding excessive noise.  
- **Linearity:** Must not clip on strong near reflections; allow basic gain control or padding if required.  
- **Reference Input:** Accept a stable copy of the transmit chirp for mixing.  
- **Beat/IF Band:** Output a low-kHz beat signal; include basic filtering to remove DC offset and avoid aliasing into the ADC.  
- **Impedance & Layout:** Maintain 50 Ω paths and good physical separation to limit leakage.  
- **Dynamic Range:** Able to handle weak and strong reflections without major adjustment. 
