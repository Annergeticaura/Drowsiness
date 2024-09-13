# Drowsiness
Drowsiness detection with GUI
# Drowsiness Detection Model
Overview
This project is aimed at detecting whether individuals in a vehicle are asleep or awake based on images or video input. The system is designed to identify multiple people in a single image or video frame and determine how many are sleeping. If a person is detected as sleeping, the system marks them in red and predicts their age. Additionally, a pop-up message is displayed, indicating the number of sleeping people and their ages.

# Features
Detects multiple people in an image or video.
Identifies whether a person is awake or asleep.
Marks sleeping individuals in red within the video or image preview.
Predicts the age of sleeping individuals using a pre-trained age detection model (ResNet50).
Pop-up message shows the number of sleeping individuals and their predicted ages.
Includes a GUI for both image and video input preview.
# Technologies Used
Python (v3.x)
TensorFlow / Keras: For building the custom CNN model for drowsiness detection and the pre-trained ResNet50 for age prediction.
OpenCV: For video/image processing.
Tkinter: For building the graphical user interface (GUI).
NumPy: For numerical operations.
Matplotlib: For visualizing predictions.
Model Architecture
# Drowsiness Detection Model
A custom Convolutional Neural Network (CNN) was designed for binary classification (awake or drowsy). The architecture consists of:

Four Conv2D layers with increasing filters (32, 64, 128, 256), each followed by Batch Normalization and MaxPooling.
Flattening the output after convolution layers.
Two Dense layers (512 and 128 units) with Dropout layers to reduce overfitting.
Sigmoid activation for binary classification (drowsy or awake).
# Age Detection Model
For age detection, the project utilizes a ResNet50 model pre-trained on ImageNet, with a custom dense layer added for regression on the UTK dataset. This model predicts the age of individuals who are detected as drowsy.
# Dataset
The model was trained using an in-house dataset consisting of labeled images with either eyes or mouths captured in open or closed states. The dataset is split into train, validation, and test sets to ensure accurate model performance. For age detection, the UTKFace dataset was used, which contains images of faces labeled with age.
# License
This project is under MIT license
