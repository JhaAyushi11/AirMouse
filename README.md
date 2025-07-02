# 🖱️ AirMouse - Control Your Mouse with Hand Gestures

**AirMouse** is a Python-based virtual mouse system that uses real-time hand gesture recognition via webcam to perform mouse actions. Built using **MediaPipe** for hand tracking and **OpenCV** for video processing, it enables touch-free control of your system.

---

## ✨ Features

- 🖱️ Move the mouse using your index finger
- 👈 Perform a left click using gestures
- 👉 Perform a right click using gestures
- 👆 Double-click with combined finger gestures
- 📸 Capture screenshots using a specific hand pose
- 🔃 Scroll up or down with finger movements
- 🔍 *(Zoom gestures are coded but currently commented out)*

---

## 🛠️ Tech Stack

- **Python 3.x**
- **OpenCV**
- **MediaPipe**
- **PyAutoGUI**
- **Pynput**
- **NumPy**

---

## 🧠 How It Works

- Uses **MediaPipe** to track 21 hand landmarks.
- Computes angles between finger joints via `util.py` to identify gestures.
- Maps specific hand poses to mouse actions:
  - Mouse movement is controlled by the position of the index finger.
  - Gestures are interpreted using angle thresholds and relative distances between fingers.

---

**🖐️ Gesture Mappings**
Gesture	Action

Index finger only	Move mouse

Index + Thumb pinch	Left click

Middle + Thumb pinch	Right click

Thumb + Index + Middle pinch	Double click

Thumb close to Index & Middle	Take screenshot

Index above/below Middle	Scroll up/down

**📁 Project Structure
**

AirMouse/
│
├── gesture_controlled_mouse.py  # Main gesture control script

├── util.py                      # Utility functions for angles and distances

├── requirements.txt             # Python dependencies

├── .gitignore                   # Ignores virtual environment folders

├── README.md                    # Project documentation

└── LICENSE                      # Project license

**📄 License**

This project is licensed under the MIT License — feel free to use, modify, and distribute it.

💡 **Credits**
Developed by Ayushi Jha

Powered by MediaPipe and OpenCV

## 🚀 Installation

```bash
git clone https://github.com/JhaAyushi11/AirMouse.git
cd AirMouse
python -m venv newenv
newenv\Scripts\activate  # For Windows
pip install -r requirements.txt
