# AnomalyDetection
This is the sub-project of Industry-University Cooperation for implementing the anomaly detection.

## project preview
![Select_AdobeExpress](https://user-images.githubusercontent.com/43237393/174948802-0b33d1e6-2c9d-4a82-be88-3cc7d707d1a8.gif)

## Functionality
1. Select the region of interest
2. Detect any Anomaly(movement)
3. Predict the anomaly whether it is human activity or unknown activity

## Requirements

We use yolov5 to detect whether the movement is human or not. (see more detail in [here](https://docs.ultralytics.com/tutorials/pytorch-hub/))
```
$ pip install -r https://raw.githubusercontent.com/ultralytics/yolov5/master/requirements.txt
```

The pytorch and openCV installment is dependent on your OS and python version.
(In my case, use m1 macOS and miniforge virtual environment)
```
$ pip3 install torch torchvision torchaudio
$ pip3 install opencv-python
```

## Getting start
Python file execute
```
python3 ./AnomalyDetection.py
```

edit VIDEO_PATH for testing the other video
```python
VIDEO_PATH = 'video/sample.mp4'
```
to custom

if you want to detect in realtime on your webcam, modify VideoCapture ID to catch your webcam. (ID can be diverse depending on your OS and system)
```pythonse
cap = cv2.VideoCapture(0)
```
