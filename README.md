
# FFT32: 32-Point Fast Fourier Transform in C

A simple, C-callable implementation of a **32-point Fast Fourier Transform (FFT)** function.  
This module processes complex input data using a radix-2 FFT algorithm, designed for DSP applications, signal processing education, and embedded projects.

---

## 🚀 Features

- Standard C implementation: portable, no platform dependency
- Accepts arbitrary number of points (parameterized for 32 by default)
- Efficient radix-2 FFT computation
- In-place calculation: input array overwritten with FFT output
- Includes bit reversal for data reordering
- Suitable for DSP, audio, and scientific applications

---

## 📂 Files

- FFT32.c  : 32-point C-callable FFT function (`void FFT32(COMPLEX *Y, int N)`)
- Requires a twiddle factor array: `COMPLEX w[PTS]` (to be defined externally)

---

## 🛠️ Usage Example

#define PTS 32
COMPLEX data[PTS];
// ... fill data with real/imag samples ...
FFT32(data, PTS);
// data[] now contains the FFT output

Twiddle factors (`w[]`) must be initialized before calling FFT32.

---

## 📝 License

Open-source.  
You can use, modify, and share freely for research or education.

---

## 👨‍💻 Author

Originally created by DSPlab.  
Packaged and documented for modern use by Doğukan Avcı (https://github.com/AvciDogukan).

---
