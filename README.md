# Yoga Pose Detection Using TensorFlow and Streamlit UI

## Overview
This project demonstrates a Yoga Pose Detection system using the MoveNet model (TensorFlow Lite) for pose estimation. The notebook processes yoga pose images, identifies key points, and classifies poses, providing visual feedback.

## Repository Structure
- **YogaPoseDetection.ipynb**: The main Jupyter Notebook containing the code for pose detection and classification.
- **requirements.txt**: List of Python dependencies required to run the notebook.
- **treepose.jpg**: Sample image used to test the pose detection model.
- **README.md**: Documentation for the project.

## Approach
### Data Preprocessing
1. Input images are resized to 192x192 pixels, as required by the MoveNet model.
2. The images are normalized and converted into tensors for model input.

### Model Architecture
- **MoveNet (SinglePose Lightning)**:
  - Pre-trained TensorFlow Lite model for high-performance pose estimation.
  - Outputs coordinates and confidence scores for detected key points.

### Visualization
- Key points and skeletal connections are overlaid on the original image using OpenCV for visualization.
- The notebook provides visual feedback on the detected poses and confidence levels.

### Pose Classification
- A rule-based approach is used to classify poses based on the relative positions of key points (e.g., head, shoulders, hips).
- Poses included in the classification: *Tree Pose*, *Downward Dog*, etc.

## Getting Started
### Prerequisites
- Python 3.8+
- Jupyter Notebook
- Required libraries: TensorFlow, TensorFlow Hub, OpenCV, NumPy, and Pillow.

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

3. Open the Jupyter Notebook:
    ```bash
    jupyter notebook YogaPoseDetection.ipynb
    ```

4. Run the notebook cells step by step to see the results.

## Results
- The notebook provides annotated visualizations of detected poses.
- Confidence scores indicate the reliability of the detected key points.

### Example Output
- **treepose.jpg**:
  - The pose detection model successfully identifies key points and overlays a skeleton on the original image.
  - Pose: Tree Pose
  - Confidence: High

## Next Steps
- Enhance classification using a machine learning-based model for better accuracy.
- Extend support for real-time pose detection using live camera feeds.
- Add more complex yoga poses to the classification system.

## License
This project is open-source and available under the MIT License.

## Acknowledgments
- TensorFlow Hub for the MoveNet model.
- The Yoga Pose Dataset community for inspiration.
