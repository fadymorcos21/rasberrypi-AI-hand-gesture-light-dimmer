# Hand Gesture Light Dimmer

An experimental Raspberry Pi–based home light dimmer controlled entirely by hand gestures using AI-powered computer vision.

This project tracks your hand with a webcam, calculates the distance between your thumb and index finger to set brightness (0–100%), and locks in the level with a thumbs‑up gesture.

> **Work in Progress**: Core detection and gesture logic are in place. Ongoing work includes calibration, performance tuning, and hardware integration for signal output.

---

## 🛠️ Key Features

- **Hand Detection & Tracking**: Real‑time landmark detection via MediaPipe.
- **Gesture‑Based Brightness**: Maps thumb–index distance linearly to brightness percentage.
- **Confirmation Gesture**: Thumbs‑up gesture confirms and sends the brightness command.
- **Activation & Reset**:
  - **Activate**: Show an open palm to enter adjustment mode.
  - **Reset**: Lower your hand or make a closed fist to exit.

---

## ⚙️ How It Works

1. **Activation**  
   Show an open palm in view of the webcam to enter brightness adjustment mode.

2. **Measurement**  
   Move your thumb and index fingertip apart; the system measures the Euclidean distance and maps it to 0–100%.

3. **Confirmation**  
   Give a thumbs‑up gesture to lock in the chosen brightness value and trigger the dimming command.

4. **Reset/Exit**  
   Lower your hand or make a closed fist to exit adjustment mode and stop sending commands.

---

## 📦 Prerequisites

### Hardware

- Raspberry Pi (4 or 5 recommended)
- USB webcam
- AI accelerator (Hailo AI Hat or compatible)
- *Pending*: Hardware module or interface to relay brightness commands to your light source (e.g., GPIO, I2C LED driver)

### Software

- Raspberry Pi OS (64‑bit)
- Python 3.9+
- OpenCV
- MediaPipe
- NumPy

---

## 🔧 Installation & Setup

Project is still incomplete, this information will come soon

---

## 🛣️ Roadmap / TODO

- [ ] Integrate AI accelerator for MediaPipe inference
- [ ] Select and interface hardware module for light control (GPIO or external driver)
- [ ] Implement calibration routine for varying camera distances
- [ ] Optimize performance (frame rate, latency)
- [ ] Add GUI overlay for live brightness feedback

---


## 🙏 Acknowledgments

- MediaPipe for hand-tracking.
- OpenCV community for Python bindings and examples.
- Hailo AI for edge acceleration hardware.
