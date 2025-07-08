# Frequency-Domain Image Fusion and Audio Restoration using DFT

This project explores the use of **Discrete Fourier Transform (DFT)** and **digital filtering techniques** for enhancing multimedia signals in both the visual and acoustic domains. It consists of two key modules:

- **Image Frequency Mixer**: Combines high- and low-frequency content from two images to create a perceptual hybrid image.
- **Audio Frequency De-Mixer**: Removes intrusive audio frequencies (e.g., a piccolo) using a band-stop filter in the frequency domain.

---

## Project Overview

### 1. Image Frequency Mixer
Inspired by perceptual illusions like the Einstein-Monroe hybrid, this module fuses:
- Low-frequency content from one image (e.g., dog)
- High-frequency detail from another (e.g., cat)

Techniques used:
- 2D FFT and `np.fft.fft2`
- Gaussian low-pass & high-pass filters
- Frequency-domain masking and inverse FFT reconstruction
- Filter visualization and frequency response plots

### 2. Audio Frequency De-Mixer
Designed to suppress unwanted instrumental components using digital filter design and spectral analysis.

Techniques used:
- 1D FFT and log-magnitude spectrum visualization
- Chebyshev Type II IIR band-stop filter (`scipy.signal.cheby2`)
- Zero-phase filtering via `filtfilt`
- Waveform and frequency-domain comparison plots
- Audio export via `soundfile`

---

## Objectives

- Leverage DFT and FFT to analyze and manipulate signals in the frequency domain
- Apply filter design theory from Signals & Systems to practical problems
- Implement image fusion and audio denoising pipelines using Python

---

## Technologies & Libraries

- Python 3.x
- NumPy
- SciPy
- Matplotlib
- OpenCV (for image processing)
- Pillow (PIL)
- SoundFile (for WAV output)

---

## Results

- Generated hybrid images where different content is visible at different viewing distances
- Successfully removed high-frequency noise (1kHz–10kHz) from audio using zero-phase IIR filters
- Validated results with frequency spectra, waveform comparisons, and visual filter responses

---
