# BH Merger Waveform Explorer (Pedagogical)
## Author
Gianluca Inguglia (Marietta Blau Institute, Austrian Academy of Sciences, Vienna)

# Scope
Interactive, browser-based applet to explore how a compact-binary black-hole merger waveform changes with parameters.

Live demo (GitHub Pages):
- https://ginguglia.github.io/bh-waveform-applet/

## What it does
- Generates a **fast, pedagogical IMR-like** time-domain waveform:
  - inspiral chirp (Newtonian-inspired frequency evolution),
  - smooth merger boost,
  - damped ringdown.
- Lets users tune:
  - component masses (m1, m2),
  - distance,
  - inclination,
  - coalescence time and ringdown time,
  - sample rate and window length.
- Provides a **“detector view”** via a simple hard bandpass in frequency space:
  - choose presets (aLIGO-ish, ET-ish, etc.) or set custom f_low / f_high.

## Intended use
This is an **outreach / intuition / teaching** tool.
It is **not** a substitute for waveform models used in data analysis.

For real analyses, use LALSuite waveform families (e.g. IMRPhenom, SEOBNR) and proper detector response, PSD whitening, calibration, etc.

## How it works
- Single static file: `index.html`
- Plotting: Plotly.js (CDN)
- Bandpass: simple FFT (radix-2) with hard frequency cutoffs

## Embed on a website
In your website builder, embed as a URL/iframe:

- https://ginguglia.github.io/bh-waveform-applet/

## License

- CC BY 4.0 (for educational content)


## Notes / limitations
- The waveform amplitude is **arbitrarily scaled** for visualization.
- The bandpass is a **toy model** of detector bandwidth (not a full interferometer response).
- Some presets are illustrative and may not match official sensitivity curves.
