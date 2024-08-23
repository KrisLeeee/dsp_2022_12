# dsp_2022_12


# Digital Signal Processing Final Project

## Image Tracking Using Correlation Filters

This project was developed as the final assignment for the Digital Signal Processing course. It focuses on implementing an image tracking system using correlation filters in Python, utilizing the `numpy` and `cv2` libraries.

### Project Overview

The objective of the project is to track objects in video frames, specifically focusing on a human subject in a surfing video. The tracking is conducted on both the full body and the head of the subject. The system draws a bounding box around the human figure and tracks the object across different frames.

### Default Settings

- **Video Source**: Surfing man video
- **Tracking**: Full body and head
- **Color Filter**: Grayscale
- **Output**: Bounding box around the tracked object

### Performance Enhancements

To improve the tracking performance, several strategies were employed:

1. **Hyperparameter Adjustments**
   - *Learning Rate, Variance, Pre-Training Frame Numbers*: Fine-tuned to optimize tracking accuracy.
   - *Ground Bounding Box*: Adjusted to be wider, allowing better coverage of body parts, especially when the subject rotates.

2. **Filter Criteria Adjustments**
   - *Color Space Conversion*: Switching from the default grayscale to HSV improved performance in partial body tracking. This enhancement is due to the clear color contrast between the blue sea and the relatively red human skin, making it easier for the algorithm to distinguish and track the human subject.
   - *Filter Recentralization*: Based on the initial frame, this technique prevents the target from drifting out of the bounding box during tracking, thereby enhancing the recognition of specific body parts, particularly the legs.

### Results

- **HSV Only**: Improved performance in partial body tracking.
- **Filter Recentralization Only**: Enhanced performance in recognizing and tracking specific body parts, particularly the legs.
- **HSV + Filter Recentralization**: 
  - Achieved the best performance in full-body tracking.
  - Slightly reduced accuracy in head tracking.

---

This version now includes detailed explanations for why HSV and filter recentralization improved performance, making your project description even more informative and professional.
