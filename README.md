# Face Landmark Detection using MediaPipe

## Overview
This project utilizes OpenCV and MediaPipe to detect facial landmarks from an image. The function extracts and processes facial key points, optionally drawing them on the image.

## Features
- Detects facial landmarks using MediaPipe's FaceMesh.
- Extracts X, Y, and Z coordinates of facial key points.
- Optionally draws the facial landmarks on the input image.
- Supports static image mode for better landmark detection.

## Requirements
Ensure you have Python installed along with the required dependencies:

```bash
pip install opencv-python mediapipe
```

## Usage
### Import and Use the Function
```python
import cv2
from your_script import get_face_landmarks

# Load an image
image = cv2.imread("face.jpg")

# Get facial landmarks
landmarks = get_face_landmarks(image, draw=True)

# Display the image with landmarks drawn
cv2.imshow("Face Landmarks", image)
cv2.waitKey(0)
cv2.destroyAllWindows()
```

## How It Works
1. The input image is converted to RGB format for MediaPipe processing.
2. MediaPipe's FaceMesh model detects facial landmarks.
3. X, Y, and Z coordinates of each landmark are extracted and normalized.
4. If `draw=True`, the landmarks are drawn on the image.

## Technologies Used
- **OpenCV** - For image processing and visualization.
- **MediaPipe** - For facial landmark detection.



