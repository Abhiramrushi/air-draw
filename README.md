# Air Canvas – Hand Gesture Drawing App

**Creator:** abhiram

Air Canvas turns your webcam into an invisible paintbrush. Wave your hand in mid-air and watch smooth digital ink appear in real time, powered by OpenCV for video capture and MediaPipe Hands for landmark tracking.

## Features
- **Real-time Performance Monitoring**: Live overlay of system latency (ms) and FPS for performance evaluation.
- **Accuracy Tracking**: Display of MediaPipe's hand tracking confidence score.
- **Air-Writing & Canvas**: High-precision hand landmark detection for smooth digital interaction.
- **Gesture Control**: 
  - **Draw**: Index finger extended (green cursor).
  - **Pause**: Fist (red cursor).
  - **Clear**: Open palm (yellow cursor).
- **Digital Interaction**: Press `s` to save your "air-writing" or drawings as PNG files.
- Dual-window display: Augmented webcam feed plus a dedicated canvas view.

## Performance Evaluation
The system includes built-in metrics to evaluate efficiency and reliability:
- **System Latency**: Measured as the time taken to process each frame (from capture to display).
- **Recognition Accuracy**: Represented by the MediaPipe confidence score (0.0 to 1.0), indicating how reliably the hand is detected.
- **Stability**: Point smoothing (Momentum-based) and gesture filtering reduce jitter and accidental triggers.

## Gesture Mapping
| Gesture | Pose | Action |
| --- | --- | --- |
| **Draw** | Index finger up, others folded | Paint continuous strokes |
| **Pause** | All fingers folded (Fist) | Stop painting |
| **Clear** | All fingers extended (Palm) | Reset the canvas |
| **Save** | Press 's' key | Save current canvas to file |
| **Quit** | Press 'q' key | Exit application |

## Tips & Troubleshooting
- Ensure good, even lighting so MediaPipe can detect landmarks reliably.
- If the wrong gesture triggers, keep your hand within the frame and slow down transitions between poses.
- Strokes follow the index finger tip; move the whole hand rather than bending only the finger for smoother curves.
- If the webcam cannot be opened, close other apps that may be using it and rerun `python main.py`.

## Folder Structure
```
air-canvas/
├── main.py              # Application entry point & UI loop
├── gesture_detector.py  # MediaPipe Hands wrapper + gesture logic
├── canvas.py            # Canvas class for persistent drawing
├── utils.py             # Helper utilities for rendering overlays
├── requirements.txt     # Runtime dependencies
└── README.md            # Project guide
```

Add your own screenshots or GIFs of the running app directly to this README to showcase results.



