An experimental Raspberry Pi–based light home dimmer controlled by hand gestures using AI-powered computer vision. This project tracks your hand with a webcam, measures the distance between your thumb and index fingertip to set brightness, and confirms the selected level with a thumbs-up gesture.

Work in progress: Core functionality is implemented, but calibration, performance optimization, and hardware integration are ongoing.


Hand Detection & Tracking: Leverages MediaPipe to detect hand landmarks in real time.

Gesture-Based Control: Measures thumb–index distance to calculate brightness percentage.

Confirmation Gesture: Uses a separate thumbs-up gesture to lock in the brightness level.

How It Works

Activation: Show an open palm to activate the brightness adjustment mode.

Measurement: Move your thumb and index finger—distance is mapped linearly to 0–100% brightness.

Confirmation: Give a thumbs-up to confirm the new brightness level and send the command to the light source.

Reset: Lower your hand or show a closed fist to exit adjustment mode.


Prerequisites

Hardware:

Raspberry Pi (Pi 4/5 recommended)

USB webcam

Hailo AI Hat or compatible accelerator

Still need to decide for hardware to recieve single and control the light dimmer

Software:

Raspberry Pi 5 OS (64-bit)

Python 3.9+

OpenCV

MediaPipe

NumPy



Roadmap / TODO:
- Need to determine how to leverage AI accelarator with mediea pipe hand detection
- Determine hardware for signal reciever to set light brightness level
