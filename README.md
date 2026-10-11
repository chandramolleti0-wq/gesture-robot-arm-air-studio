#  Gesture Robot Arm Air Studio

**A gesture-controlled virtual drawing and air-writing application powered by Python, OpenCV, and MediaPipe.**

Draw in the air using your webcam, recognize handwritten letters and numbers, identify geometric shapes, and save your digital artwork — all with real-time hand tracking.

##  Features

- **Real-Time Hand Tracking** — Detects hand landmarks through your webcam using MediaPipe.
- **Virtual Drawing Canvas** — Draw using your index finger without a physical mouse.
- **Air Writing** — Write individual English letters and numbers in the air.
- **Character Recognition** — Recognizes uppercase letters (A–Z) and digits (0–9) using OpenCV template matching.
- **Shape Recognition** — Detects common shapes, including triangles, squares, rectangles, pentagons, hexagons, circles, and stars.
- **Multiple Brush Colors** — Switch colors and adjust brush size.
- **Undo and Clear** — Undo drawing actions or clear the canvas.
- **Save Drawings** — Save your artwork locally.
- **Local Processing** — No external AI API is required for the implemented drawing and recognition features.

## Tech Stack

| Technology | Purpose |
|---|---|
| Python 3.12 | Application logic |
| OpenCV | Image processing, drawing, and template matching |
| MediaPipe | Real-time hand landmark detection |
| NumPy | Image and numerical operations |
| Visual Studio Code | Development environment |

## 📋 Requirements

- Windows 10 or Windows 11
- Python 3.12 (64-bit recommended)
- A working webcam
- Internet connection for initial package installation

## ⚙️ Installation

### 1. Clone the repository

```bash
git clone https://github.com/chandramolleti0-wq/gesture-robot-arm-air-studio.git
cd gesture-robot-arm-air-studio
```

### 2. Create a virtual environment

```powershell
py -3.12 -m venv .venv
```

### 3. Install the dependencies

```powershell
.\.venv\Scripts\python.exe -m pip install --upgrade pip
.\.venv\Scripts\python.exe -m pip install opencv-python mediapipe==0.10.21 numpy
```

### 4. Run the application

```powershell
.\.venv\Scripts\python.exe air_studio.py
```

Allow camera access if Windows requests permission.

## Keyboard Controls

| Key | Function |
|---|---|
| `1` – `5` | Change brush color |
| `+` / `-` | Increase or decrease brush size |
| `Enter` | Recognize both character and shape |
| `L` | Recognize a letter or number |
| `H` | Recognize a shape |
| `C` | Clear the canvas |
| `U` | Undo the last drawing action |
| `S` | Save the drawing |
| `Q` | Quit the application |

## How to Use

1. Launch the application.
2. Position your hand in front of the webcam.
3. Raise only your index finger to draw on the digital canvas.
4. Move your finger to write a letter, number, or draw a geometric shape.
5. Press `L` to recognize the character or digit.
6. Press `H` to recognize the shape.
7. Press `Enter` to run both recognition functions.
8. Press `S` to save your drawing.

**Tip:** Draw one large, centered letter or number at a time for better recognition results.

## How Recognition Works

### Character Recognition

The application compares the normalized drawing against character templates generated with OpenCV fonts. It supports uppercase English letters and digits.

This is a lightweight template-matching prototype, not a trained OCR or deep-learning model. Handwriting styles, cursive text, and multiple connected characters may reduce accuracy.

### Shape Recognition

The application uses contour detection and polygon approximation to identify common geometric shapes. Results depend on how clearly the shape is drawn.

## Project Structure

```text
gesture-robot-arm-air-studio/
├── air_studio.py
├── main.py
├── main_mouse_paint.py
├── config.py
├── requirements.txt
├── README.md
├── AIR_STUDIO_SETUP.md
├── apps/
├── perception/
├── tests/
├── controllers/
├── worlds/
└── .gitignore
```

*Note: The exact files and directories depend on the version of the project you have downloaded.*

## Privacy

The implemented Air Studio features process camera frames locally. The application does not require an external AI API for drawing, character template matching, or shape recognition.

## Future Enhancements

- Improve handwriting recognition using a trained machine-learning model.
- Support complete words and connected handwriting.
- Add voice-controlled drawing.
- Integrate gesture recognition with a physical robotic arm.
- Add more drawing tools and export formats.

## Author

**Chandra Sekhar Molleti**

- GitHub: [@chandramolleti0-wq](https://github.com/chandramolleti0-wq)
- LinkedIn: [Chandra Sekhar Molleti](https://linkedin.com/in/chandrasekarmolleti)

## License

This project is licensed under the **MIT License**. See the [LICENSE](LICENSE) file for details.

---

⭐ If you find this project useful, consider giving the repository a star!
