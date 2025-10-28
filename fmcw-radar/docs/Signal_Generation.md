### Signal Generation

Generates the 2.4 GHz frequency sweep used for radar transmission.  
Must produce a stable, repeatable chirp fully contained within the ISM band for reliable range measurements.

- Operates only within **2.400–2.4835 GHz** ISM band.  
- Sweep width up to **80 MHz**.  
- Output power **0 – +10 dBm** into **50 Ω**.  
- Chirp time adjustable **1 – 10 ms**.  
- Start marker jitter **< 1 µs** for timing sync.  
- Controlled by **FPGA or Raspberry Pi** via SPI or simple digital lines.  
- Stable frequency reference (**a few ppm**) to maintain consistent range readings.  
- All emissions remain inside the ISM band and **below 100 mW EIRP**.