# Virtual Mouse - Computer Vision

<!-- <div align="center">
    <img src="xy" alt="Banner" width="1080" />
</div> TODO: UPDATE PHOTO OF VIRTUAL MOUSE-->

## Description

**Virtual Mouse** uses hand detection technology to allow users to control their computer using simple hand gestures. By leveraging **OpenCV** and **MediaPipe**, this tool offers an intuitive and responsive interface for gesture-based mouse control and interaction.

## Features

- **Real-Time Hand Tracking**: Detects and tracks hand movements in live camera feed.
- **Gesture-Based Mouse Control**:
  - **Moving Mode**: Navigate the cursor by moving your hand.
  - **Clicking Mode**: Perform mouse clicks by pinching fingers together.
- **Adaptive Parameters**: Configure settings such as detection sensitivity, frame reduction, and motion smoothing for personalized use.
- **Frame Rate Display**: Provides real-time FPS feedback for performance monitoring.
- **Visual Feedback**: Displays detected hand markers and gestures on the screen.

## How It Works

### Initialization
1. **Hand Detector Setup**: Configured using parameters like:
   - **Mode**: Continuous tracking or static frame detection.
   - **MaxHands**: The maximum number of hands to detect.
   - **Complexity**: Adjusts processing detail and speed.
   - **DetectionCon**: Controls detection sensitivity.
   - **TrackCon**: Determines tracking accuracy.
2. **Camera Setup**: Adjusts resolution and frame settings for optimal performance.

### Hand Detection
1. **`findHands` Function**:
   - Converts camera feed to RGB.
   - Uses **MediaPipe** to detect hands and draw markers on joints.
2. **`findPosition` Function**:
   - Extracts joint positions and calculates the bounding box around the hand.

### Mouse Control
1. **Moving Mode**:
   - Converts hand coordinates to screen coordinates for smooth cursor navigation.
   - Uses motion smoothing to enhance user experience.
2. **Clicking Mode**:
   - Monitors the distance between two fingertips.
   - Simulates a mouse click when the distance is below a threshold.

### Gesture Analysis
- **`fingersUp` Function**:
  - Determines which fingers are raised.
  - Enables gestures for mode switching and tool selection.
- **`findDistance` Function**:
  - Calculates the distance between two joints for advanced gesture inputs.

## Applications

- **Gesture-Controlled Mouse**: Navigate and click on your screen with hand gestures.
- **Interactive Systems**: Integrate into smart homes or AR/VR setups for hands-free control.
- **Assistive Technologies**: Provides an accessible solution for users with limited mobility.


### A video demonstration of this project in action will be uploaded soon.

****
