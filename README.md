## Real-Time Hand Gesture Recognition using CVZone

### Overview

This Python script utilizes the CVZone library for real-time hand gesture recognition. The code detects hand gestures captured through a webcam and classifies them into predefined categories such as "Down", "Up", "Right", "Back", "Left", and "Front". The hand gestures are detected using computer vision techniques and classified using a pre-trained model from Google's Teachable Machine. 

![Real Time Detection](real-time-detection(cvzone).jpg)

### Requirements

- Python 3.x
- OpenCV (cv2)
- CVZone
- NumPy
- Math module

### Setup

1. Ensure you have Python installed on your system.
2. Install the required libraries using pip:

   ```bash
   pip install opencv-python cvzone numpy
   ```

3. Download the pre-trained model and labels file (keras_model.h5 and labels.txt) from the Google Teachable Machine platform or another suitable source.
4. Place the downloaded files in the same directory as the Python script.

### Usage

1. Run the Python script.
2. Ensure that your webcam is connected and functioning properly.
3. A window will open displaying the live webcam feed with hand gesture recognition overlay.
4. Perform hand gestures in front of the webcam.
5. The recognized gesture will be displayed on the screen along with a bounding box around the detected hand.

### Readme

The script uses CVZone, an open-source computer vision library, for hand detection and classification. It captures video input from the webcam and processes it frame by frame. The HandDetector class from CVZone is used to detect hands in the video stream, while the pre-trained model loaded using the Classifier class is employed to classify the hand gestures.

#### Important Components:

- **Hand Detection**: The HandDetector class is used to find hands in each frame of the video stream. It returns the bounding box coordinates of the detected hands.
- **Gesture Classification**: The pre-trained model loaded from 'keras_model.h5' and 'labels.txt' is used to classify the hand gestures. The model predicts the label corresponding to each detected hand gesture.
- **Image Preprocessing**: The captured hand region is resized and aligned to a standard size before being fed into the classification model.
- **Visualization**: The recognized gesture label and a bounding box around the detected hand are overlaid onto the video feed for visualization purposes.

### Dataset

The dataset used to train the hand gesture recognition model can be found on Kaggle at the following link: [Hand Gesture Recognition Dataset](https://www.kaggle.com/datasets/grassknoted/asl-alphabet).

### Credits

- CVZone: [GitHub Repository](https://github.com/cvzone/cvzone)
- Google Teachable Machine: [Platform](https://teachablemachine.withgoogle.com/)

For any questions or feedback, please contact [sousannahabdalla@gmail.com].
