### Visualisation

Renders the live 2D top-down radar map on a display.

- **Input:** Receive framed spokes (angle + range bins) from FPGA.
- **Render:** Polar plot (range vs angle) updating continuously.
- **Update rate:** Smooth display at normal scan speeds.
- **Startup:** Auto-launch on boot; connect and draw without user input.
- **Platform:** Raspberry Pi (Python), HDMI.
- **Status:** Basic on-screen indicators.
