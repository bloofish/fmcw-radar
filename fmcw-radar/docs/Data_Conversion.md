### Data Conversion (ADC)

Digitises the low-frequency beat signal from the receiver so the FPGA can process range profiles.

- **Input:** Single IF/beat signal (low-kHz band), nominal 50 Ω source; AC-coupled into ADC.
- **Sample rate:** ≥ 100 kS/s (headroom to 200–500 kS/s is fine for shorter chirps).
- **Resolution:** ≥ 12-bit effective to preserve weak returns alongside strong near targets.
- **Input range:** Scaled so typical IF sits at ~30–70% of full-scale; avoid clipping on close targets.
- **Filtering:** Simple anti-alias low-pass before ADC; high-pass to reduce DC/leakage.
- **Sync:** Start sampling on/after the chirp start marker; consistent timing each chirp.
- **Interface to FPGA:** Simple SPI or parallel output; stable clock provided to/from FPGA.
- **Throughput:** Continuous capture of one “spoke” per chirp; buffer per-chirp frame for the FPGA.
- **Power:** Runs from local 3.3 V/5 V regulation; keep analog and digital grounds well managed.
- **Test hooks:** IF test point pre-ADC and a digital test pattern/loopback mode for bring-up.
