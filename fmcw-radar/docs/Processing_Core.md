### Processing Core

Processes each chirp into a range profile and streams the results to the host PC in real time.

- **Chirp sync:** Use the chirp start marker to begin sampling and processing consistently each chirp.
- **Capture:** Store a fixed number of ADC samples per chirp.
- **FFT:** Perform a range FFT on each chirp; convert to magnitude.
- **Range bins:** Output only the useful bins (near DC removed).
- **Angle tag:** Attach the current rotation angle to each spoke.
- **Throughput:** Maintain one processed spoke per chirp and complete a full 360° scan within 2 seconds.
- **Host link:** Send formatted spoke data to the host PC over a simple wired link.
- **Clocking:** Keep timing consistent across capture and processing to avoid slips or missing data.
