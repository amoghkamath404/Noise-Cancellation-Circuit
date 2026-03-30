
# 🎧 Active Noise Cancellation using LMS Algorithm (Simulink)

## 📌 Overview

This project demonstrates an **Active Noise Cancellation (ANC)** system implemented in **MATLAB Simulink** using the **Least Mean Squares (LMS) adaptive filtering algorithm**.

The system removes noise from a corrupted signal by estimating and subtracting unwanted noise components, producing a cleaner output signal.

---

## 🚀 Objectives

* To understand adaptive filtering using LMS algorithm
* To simulate real-time noise cancellation
* To visualize noisy vs cleaned signals using scopes

---

## 🧠 Concept

Active Noise Cancellation works on the principle:

> **Noise + Anti-noise = Silence (or reduced noise)**

The LMS algorithm adaptively updates filter coefficients to minimize the error between:

* Desired signal (noisy signal)
* Estimated noise

---

## 🏗️ System Architecture

### Blocks Used:

* Sine Wave (Original Signal)
* Band-Limited White Noise (Noise Source)
* Sum Block (Signal + Noise)
* LMS Filter
* Subtraction Block (Noise Removal)
* Scope (Visualization)

---

## 🔄 Working Flow

1. Generate a clean signal using **Sine Wave**
2. Add noise using **Band-Limited White Noise**
3. Combine them to create a **noisy signal**
4. Feed noisy signal to the **LMS filter**
5. LMS estimates the noise component
6. Subtract estimated noise from noisy signal
7. Output is a **cleaned signal**

---

## ⚙️ Simulation Parameters

| Parameter   | Value                           |
| ----------- | ------------------------------- |
| Solver Type | Fixed-step                      |
| Solver      | Discrete (no continuous states) |
| Step Size   | 0.001                           |
| Stop Time   | 10–20 sec                       |

---

## 🔧 LMS Filter Parameters

| Parameter       | Value |
| --------------- | ----- |
| Step Size (μ)   | 0.01  |
| Filter Length   | 32    |
| Initial Weights | Zeros |

---

## 📊 Results

* Input signal: Noisy waveform
* Output signal: Reduced noise, smoother waveform
* Noise signal: Random, zero-mean signal

---

## 📸 Output Screenshots

> Add your scope screenshots here
> Example:
>
> * Noisy Signal (Scope 1)
> * Filtered Output (Scope 2)

---

## 📂 Project Structure

```
📁 Active-Noise-Cancellation-Simulink
│
├── anc_model.slx
├── README.md
├── screenshots/
│   ├── input_signal.png
│   ├── output_signal.png
│
```

---

## 🛠️ Requirements

* MATLAB (R2020 or later recommended)
* Simulink
* DSP System Toolbox

---

## ⚠️ Common Issues & Fixes

### 1. Empty Scope Output

* Ensure solver is set to **fixed-step discrete**
* Check sample time consistency (0.001)

### 2. LMS Not Working

* Verify correct connections:

  * Input (x)
  * Desired (d)

### 3. No Noise Reduction

* Tune step size (μ)
* Increase filter length

---

## 🎯 Applications

* Headphones (ANC technology)
* Audio signal processing
* Biomedical signal filtering (ECG noise removal)
* Communication systems

---

## 📚 References

* MATLAB Documentation
* DSP System Toolbox Guide
* Adaptive Filter Theory (Widrow & Stearns)

---

## 🙌 Author

**Amogh Kamath**

---

## ⭐ If you found this helpful

Give this repo a ⭐ on GitHub!
