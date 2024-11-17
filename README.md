# Vehicle-Tracking-and-Counting
This project implements vehicle tracking and counting using a pre-trained YOLOv8 object detection model combined with the Supervision framework. The objective is to annotate and track vehicles from a video, count them as they cross a defined line, and visualize the results with bounding boxes and confidence scores.
---

## 2. Key Concepts and Frameworks Used

### YOLOv8
- **YOLO (You Only Look Once)** is a state-of-the-art object detection model.
- It is highly efficient for real-time applications due to its speed and accuracy.
- In this project, YOLOv8 is used to detect objects like cars, buses, and motorcycles.

### Supervision Library
- A utility framework for handling annotations, drawing bounding boxes, and tracking objects.
- Provides functionality for line annotations, object tracking, and enhanced visualizations.

### ByteTrack Algorithm
- A tracking algorithm integrated with the Supervision framework to track detected objects across video frames.

### OpenCV
- Used for frame-by-frame video processing and general image manipulation.

---
## 4. Challenges and Solutions

### Challenge: Handling Overlapping Bounding Boxes
**Solution**: The ByteTrack algorithm ensures stable tracking across frames, even when objects overlap, by effectively managing object identities and maintaining consistent tracking.

### Challenge: Real-Time Inference on High-Resolution Videos
**Solution**: Model optimization using the `fuse()` method reduces latency during inference by merging batch normalization layers into convolution layers, thereby speeding up the process.

### Challenge: Filtering Relevant Classes
**Solution**: The `class_id` attribute is utilized to filter detections for specific object classes (e.g., cars, buses, motorcycles), ensuring that only relevant objects are included in the analysis.

---

## 5. Results
- Successfully detected, tracked, and counted vehicles crossing the defined line in the video.
- Displayed bounding boxes with:
  - Class labels (e.g., car, bus, motorcycle).
  - Confidence scores indicating detection certainty.
  - Unique tracking IDs for objects, ensuring continuity across frames.
- Produced an annotated video showing:
  - Vehicle tracking visualizations.
  - A counting line to monitor objects as they cross.
  - High-quality, visually informative results for traffic monitoring and analysis.
