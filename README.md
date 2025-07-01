# RealTime-Virtual-Whiteboard
The project aims to create an interactive whiteboard that allows users to draw on a canvas using hand gestures. The application utilizes a webcam to capture hand movements and Mediapipe to detect and track hand landmarks for gesture recognition.

# Key Features
Color Selection: Users can select different colors (Blue, Green, Red, Yellow) for drawing by positioning their hand over specific color buttons displayed on the screen. A "CLEAR" button allows users to reset the drawing area.

Drawing Mechanism: The system tracks the position of the user's index finger to draw lines on the canvas. Drawing starts when the index finger is close to the thumb (pinching gesture).

Canvas and UI: The application displays a whiteboard area where users can draw. Color buttons and the clear button are displayed on the side of the canvas for easy access.

Real-Time Interaction: The webcam feed is processed in real-time to update the canvas with the user's drawing. Hand landmarks are detected using Mediapipe, and their positions are used to control the drawing functionality. Technical Details

Libraries Used: OpenCV: For image processing and GUI creation. NumPy: For handling image arrays. Mediapipe: For hand gesture recognition and landmark detection. deque from collections: For managing and storing drawing points efficiently.

Main Components: Color Points Handling: Different deque lists manage drawing points for each color. Gesture Recognition: Detects hand positions and gestures to perform actions like drawing and color selection.

Drawing and UI: Handles drawing on the canvas and updates the user interface in real-time.
