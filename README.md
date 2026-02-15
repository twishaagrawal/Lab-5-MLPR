# Lab-5-MLPR
Lab 5 for the Machine Learning and Pattern Recognition course

Project Aim

The objective of this project is to implement and analyze a face detection system using classical computer vision techniques. The system detects human faces in images using Haar Cascade classifiers provided by OpenCV and evaluates its performance on both single-person and group images.

Methodology

The project is implemented in Python using OpenCV and follows the steps outlined below:
1.Image Acquisition
  Input images are read using OpenCV.
  The dataset includes:
    - A single face image
    - A group photograph containing multiple individuals
2.Preprocessing
  - Images are converted from color (BGR) to grayscale.
  - Grayscale images reduce computational complexity and improve detection reliability.
3.Face Detection
  - A pre-trained Haar Cascade classifier (haarcascade_frontalface_default.xml) is used.
  - The detectMultiScale() function scans the image at multiple scales to locate faces.
  - Parameters such as scaleFactor, minNeighbors, minSize, and maxSize are tuned to          optimize detection accuracy.
4.Visualization
  - Detected faces are marked using rectangular bounding boxes.
  - The total number of faces detected is displayed on the output image.
    
Results and Visualizations

Single Face Detection
The model successfully detects a single face in the image and draws a bounding box around it.

Group Face Detection
The model detects multiple faces in a group photograph and marks each detected face.
Total number of faces detected: 30

Key Findings
- Haar Cascade classifiers perform well for frontal faces under good lighting conditions.
- Detection accuracy decreases when:
    - Faces are partially occluded
    - Lighting conditions are poor
    - Faces are rotated or very small in size
- Group images require careful tuning of detection parameters to minimize false positives.

Conclusion
This project demonstrates that Haar Cascade-based face detection is an effective and computationally efficient approach for basic face detection tasks. While it performs well for controlled environments, its limitations become apparent in complex real-world scenarios. Modern deep learning-based methods provide higher robustness and accuracy; however, Haar Cascades remain a strong baseline for understanding classical computer vision pipelines.

Technologies Used
- Python
- OpenCV
- NumPy
- Jupyter Notebook
