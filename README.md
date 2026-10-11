# RealTime Virtual Whiteboard

Draw on a virtual whiteboard in the air using hand gestures. Your webcam tracks your index finger with MediaPipe and draws in real time, with no mouse or touchscreen needed.

## Features
- Real-time hand tracking (single hand)
- Air drawing with the index finger
- 4 colors: Blue, Green, Red, Yellow
- CLEAR button to reset the canvas
- Strokes shown on both the camera feed and a separate white canvas

## Tech Stack
- Python
- OpenCV
- MediaPipe
- NumPy

## Project Structure
├── main.py # entire application
├── whiteboard.png # preview image
└── README.md

## Installation
```bash
git clone https://github.com/Bipra09/RealTime-Virtual-Whiteboard.git
cd RealTime-Virtual-Whiteboard
pip install opencv-python mediapipe numpy
```

## Usage
```bash
python main.py
```

Two windows open: **Output** (webcam with landmarks) and **Paint** (canvas).

## Controls
| Action | Gesture |
|---|---|
| Draw | Extend index finger up, away from thumb |
| Lift pen (start new stroke) | Bring index fingertip down near thumb level |
| Select color / Clear | Hover index finger over a button in the top bar |
| Quit | Press `q` |

## How It Works
1. Webcam frames are mirrored and passed to MediaPipe Hands
2. Index fingertip (landmark 8) and thumb tip (landmark 4) are tracked
3. Fingertip positions are stored per color in `deque` buffers
4. Lines are drawn between consecutive points on both windows
5. Hovering over a top-bar button changes color or clears the canvas

## Notes
- Use good lighting and a plain background
- Keep your hand fully in frame, with the palm facing the camera
- Designed for a 640×480 webcam feed

## Future Improvements
- Eraser and brush size control
- Save canvas as image
- More colors
- Multi-hand support
  
## Author 👨‍💻
 [Bipra_Biswas](https://github.com/Bipra09)

## License
MIT
