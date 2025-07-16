
# 📷 Real-Time Pose Detection with MediaPipe and OpenCV

This project demonstrates real-time human pose detection using the **MediaPipe Pose** solution and **OpenCV**. It captures video from your webcam, processes each frame to detect body landmarks, and overlays the detected pose on the live video feed.

---

## 🛠️ Requirements

Make sure you have Python installed, then install the required packages:

```bash
pip install opencv-python mediapipe
```

---

## 🚀 How to Run

Save the Python script (e.g., `pose_detection.py`) and run it:

```bash
python pose_detection.py
```

The webcam window will pop up showing the live feed with pose landmarks drawn on detected people.

### 💡 Controls

* Press **`q`** to quit the application and close the webcam window.

---

## 🧠 How It Works

* **OpenCV** captures real-time video from your webcam.
* **MediaPipe Pose** detects human body landmarks in each frame.
* **Drawing utilities** from MediaPipe are used to overlay the landmark skeleton on the video.

---

## 🖼️ Sample Output

A live window showing something like this:

```
[Your Webcam Feed with Skeleton Overlay]
```

---

## 🧩 Customization

You can adjust the detection and tracking confidence thresholds here:

```python
mp_pose.Pose(static_image_mode=False, min_detection_confidence=0.5, min_tracking_confidence=0.5)
```

You may also process recorded video files by replacing `cv2.VideoCapture(0)` with a filename:

```python
cap = cv2.VideoCapture('video.mp4')
```

---

## 📚 References

* [MediaPipe Pose Documentation](https://developers.google.com/mediapipe/solutions/pose)
* [OpenCV Documentation](https://docs.opencv.org/)
