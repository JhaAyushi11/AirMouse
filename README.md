# AirMouse
Hand Gesture Controlled cursor project
# 🖱️ AirMouse - Control Your Mouse with Hand Gestures

AirMouse is a Python-based virtual mouse interface that uses hand gestures tracked via webcam to control your computer’s mouse actions. It leverages **MediaPipe** for hand tracking and **OpenCV** for video capture and rendering.

---

## ✨ Features

- 🖱️ Move mouse with index finger
- 👈 Left click gesture
- 👉 Right click gesture
- 👆 Double click gesture
- 📸 Take screenshots with gesture
- 🔃 Scroll up/down with finger gestures
- 🚫 (Zoom feature is coded but currently commented out)

---


## 🛠️ Tech Stack

- Python 3.x
- OpenCV
- MediaPipe
- PyAutoGUI
- Pynput
- NumPy

---

## 🧠 How It Works

- Uses `mediapipe` to track the hand landmarks.
- Analyzes angles between finger joints using `util.py`.
- Maps specific hand poses to mouse actions like click, move, scroll, etc.
- The mouse is moved by tracking the position of the index finger.
- Actions like click/double-click are determined based on gesture angle thresholds and distances.

---

## 🖥️ Installation

```bash
git clone https://github.com/JhaAyushi11/AirMouse.git
cd AirMouse
python -m venv newenv
newenv\Scripts\activate   # On Windows
pip install -r requirements.txt

--------
🖐️ Gesture Mappings

| Gesture                       | Action          |
| ----------------------------- | --------------- |
| Index finger only             | Move mouse      |
| Index + Thumb pinch           | Left click      |
| Middle + Thumb pinch          | Right click     |
| Thumb + Index + Middle pinch  | Double click    |
| Thumb close to Index & Middle | Take screenshot |
| Index above/below Middle      | Scroll up/down  |

---------


📁 Project Structure



AirMouse/
│
├── main.py             # Main gesture control script
├── util.py             # Utility functions for angles and distances
├── requirements.txt    # Python dependencies
├── .gitignore          # Ignores virtual environment folders
└── README.md           # Project documentation

-------------------------


📄 License
This project is licensed under the MIT License – feel free to use and modify it.

💡 Credits
Developed by Ayushi Jha
Powered by MediaPipe and OpenCV
