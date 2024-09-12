
# Powerlifting Barbell and Body Structure Tracking App

## Overview
I am a professional powerlifter and the Asian youth bench press record holder. I want to use what I've learned to improve my performance. Instead of relying on personal experience, I am more interested in understanding my body mechanics and barbell path during training. Through biomechanical analysis, I want to learn more efficient movement patterns based on my body's structure. That's why I came up with the idea to develop Titan Track. This app uses Mediapipe to process training videos of powerlifters (MP4 format) and provides a visual analysis of both the barbell movement path and the athlete's body structure during lifts. By leveraging Mediapipe's pose estimation capabilities, the app identifies key body joints and tracks their movement throughout the lift. If I have more time, I would like to use the identified key body joints for biomechanical analysis to explore what movements are more efficient for each individual, considering different joint proportions.

![pose_tracking_example.gif](https://mediapipe.dev/images/mobile/pose_tracking_example.gif) |
:----------------------------------------------------------------------: |
*Example of MediaPipe Pose for pose tracking.*                    |

![barbell_path_tracking_example.png](https://thebarbellphysio.com/wp-content/uploads/2020/03/Iron-Path-and-Keelo-bar-path-tracking-278x300.png) |
:----------------------------------------------------------------------: |
*Example of Barbell Path tracking.*                    |
## Features
- **Barbell Path Tracking**: Detects and visualizes the barbell’s movement.
- **Body Structure Detection**: Tracks key body joints (shoulders, elbows, hips, knees, etc.).
- **Biomechanical Analysis (In the future)**: Apply biomechanical analysis.
- **User-friendly Interface**: Upload an MP4 video and get visual feedback on performance.

## Installation

### Requirements
- Python 3.8+
- Mediapipe
- OpenCV
- Tkinter (for desktop UI) or Flask (for web UI) (If I get time to do this...)

## How the App Works (It should be like this -,-)

### 1. Video Input
   - The user uploads a training video in MP4 format.
   - OpenCV is used to extract frames from the video for processing.

### 2. Barbell Path Detection (Manual or Semi-Automatic)
   - **Option 1**: Manual tracking by detecting the barbell using color or shape detection.
   - **Option 2**: Semi-automatic tracking using barbell-specific object detection models, which can be improved later.

### 3. Pose Estimation with Mediapipe
   - Mediapipe’s **Pose** module is used to detect key body joints.
   - For each video frame, the following steps occur:
     1. **Frame Input**: The frame is fed into the Mediapipe Pose detection pipeline.
     2. **Joint Detection**: Key points on the lifter’s body (such as shoulders, elbows, knees, hips) are detected.
     3. **Data Storage**: The coordinates of each joint are stored for analysis and visualization.

### 4. Barbell Path and Body Joint Overlay
   - The app visualizes the detected body joints and the tracked barbell path on top of the original video.
   - Users can pause the video and inspect lift-specific metrics, such as joint angles, barbell path, and barbell velocity.

### 5. Performance Metrics
   - **Range of Motion (ROM)**: Measured based on joint positions.
   - **Barbell Speed**: Calculated from the barbell’s movement path.
   - **Joint Angles**: Real-time feedback on joint angles during each phase of the lift.

## Usage

1. **Upload Video**: Choose a video from your device.
2. **Barbell Detection**: The app automatically detects and tracks the barbell path.
3. **Body Structure Tracking**: The app overlays the joint structure and tracks it throughout the lift.
4. **Analysis**: Get feedback on performance metrics such as barbell speed, joint angles, and ROM.

## Customization

- You can adjust the parameters for barbell detection in the `config.py` file.
- You can customize the detected joints or adjust tracking accuracy by modifying the `pose_estimation.py` file.

## Contributing

Contributions are welcome! Feel free to fork this repository, submit a pull request, or open an issue.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
