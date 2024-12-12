# Yoga Pose Detection Using TensorFlow and Streamlit

## Overview
This project demonstrates a Yoga Pose Detection system using a TensorFlow Lite model for pose estimation (MoveNet) and a Streamlit application for user interaction. The application allows users to upload an image of their yoga pose and provides feedback on the detected pose.

## Features
- Detects and visualizes key points of human poses.
- Classifies poses into categories like Tree Pose, Downward Dog, Cobra Pose, etc.
- Provides feedback on pose detection confidence and classification results.

## Approach
### Data Preprocessing
1. Images are preprocessed into a 192x192 resolution, suitable for the MoveNet model input.
2. Images are converted to tensors and normalized before being passed to the model.

### Model Architecture
- The project uses the MoveNet SinglePose Lightning model from TensorFlow Hub.
- Keypoints extracted from the model include coordinates and confidence scores for each detected body part.

### Pose Classification
- Keypoints are used to classify poses based on relative positions of major joints (e.g., shoulders, hips, knees).
- Pose classification is implemented as a rule-based system for simplicity.

### Visualization
- Detected keypoints are drawn on the original image for feedback using OpenCV.

## Getting Started
### Prerequisites
- Python 3.8+
- TensorFlow, TensorFlow Hub, OpenCV, Streamlit, NumPy, and Pillow.

### Installation
1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/yoga-pose-detection.git
    cd yoga-pose-detection
    ```

2. Install dependencies:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the application:
    ```bash
    streamlit run src/main.py
    ```

4. Access the application at `http://localhost:8501` in your browser.

## Results
The system provides feedback on detected poses with visualized annotations. Example detected poses include:
- Tree Pose
- Downward Dog Pose
- Warrior Pose

## Next Steps
- Enhance the classification system using a machine learning model.
- Add support for video-based pose detection.
- Improve the robustness of pose classification for complex poses.
- Integrate real-time feedback for live yoga sessions.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Acknowledgments
- TensorFlow Hub for the MoveNet model.
- Streamlit for rapid UI development.
