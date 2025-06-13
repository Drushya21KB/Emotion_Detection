# Emotion_Detection
# Real-Time Emotion_Detection_Application Using TensorFlowLite model

This repository contains the trained model and label file used for detecting facial emotions in real-time on mobile applications. The model is trained using deep learning and converted to TensorFlow Lite for on-device inference.

## Dataset Source

We used the **[MMA Facial Expression Dataset] https://www.kaggle.com/datasets/mahmoudima/mma-facial-expression** available on Kaggle for training.


##  Files
| File           | Description                                               |
|----------------|-----------------------------------------------------------|
| `model.tflite` | Trained and optimized TensorFlow Lite model for emotion detection |
| `labels.txt`   | List of emotion labels corresponding to model outputs     |

##  Model Details

- **Architecture**: CNN-based model trained on facial expression dataset
- **Dataset**: MMA Facial Expression Dataset
- **Classes**:
Angry
Disgust
Fear
Happy
Sad
Surprise
Neutral

- **Output**: Softmax probabilities for each class


## Usage (Flutter App)

This model can be integrated into a Flutter app using the [`tflite`](https://pub.dev/packages/tflite) or [`tflite_flutter`](https://pub.dev/packages/tflite_flutter) plugin:

```dart
var res = await Tflite.loadModel(
model: "assets/model.tflite",
labels: "assets/labels.txt"
);
Use the camera feed to capture face frames and classify emotions in real time.

