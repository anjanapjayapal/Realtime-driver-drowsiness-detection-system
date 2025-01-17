# Real-time-driver-drowsiness-detection-system
A real-time drowsiness detection system designed to enhance road safety by identifying driver drowsiness through live video feed and triggering an alert when necessary.


## Description

The Drowsiness Detection System is a machine learning-based project aimed at detecting drowsiness and yawning in real-time using computer vision. The system utilizes a convolutional neural network (CNN) to classify images as drowsy or non-drowsy, based on facial features. It can also alert the user with an audio signal if drowsiness is detected.

## Table of Contents
- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Technologies Used](#technologies-used)
- [Acknowledgments](#acknowledgments)

## Installation

To get started with the Drowsiness Detection System, follow these steps:

1. **Clone the repository:**

    ```bash
    git clone https://github.com/yourusername/drowsiness-detection.git
    cd drowsiness-detection
    ```

2. **Install the required dependencies:**

    Create a virtual environment and install the dependencies using pip:

    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows use `venv\Scripts\activate`
    pip install -r requirements.txt
    ```

3. **Download Haarcascade files:**

    Ensure that you have the Haarcascade XML files for face, eye, and mouth detection. Place them in the appropriate directory specified in the code.

4. **Prepare the dataset:**

    Place your dataset in the specified directories for training (e.g., `Closed`, `No Yawn`, `Open`, `Yawn`).

## Usage

1. **Data Preparation:**

    The dataset is preprocessed and augmented to enhance the model's performance. You can preprocess the dataset using the provided functions. This includes face detection, eye detection, and mouth detection.

    ```python
    from data_preprocessing import face_for_yawn, get_data
    face_for_yawn()
    get_data()
    ```

2. **Model Training:**

    Train the model using the following script:

    ```python
    from train_model import train_model
    train_model()
    ```

3. **Real-time Drowsiness Detection:**

    Run the real-time drowsiness detection using the provided script. Ensure your camera is connected:

    ```python
    from real_time_detection import detect_drowsiness
    detect_drowsiness()
    ```

## Features

- **Real-Time Detection:** Detects drowsiness in real-time using a webcam.
- **Alerts:** Provides audio alerts when drowsiness is detected.
- **Data Augmentation:** Uses image augmentation techniques to enhance model performance.
- **Accuracy Visualization:** Plots accuracy and loss curves to evaluate model performance.

## Technologies Used

- **Python** - Programming language used.
- **OpenCV** - For image processing and face detection.
- **Keras** - For building and training the neural network model.
- **TensorFlow** - Backend for Keras.
- **Pygame** - For playing alert sounds.
- **Matplotlib** - For visualizing results.

## Acknowledgments

- [OpenCV Documentation](https://docs.opencv.org/)
- [Keras Documentation](https://keras.io/)
- [TensorFlow Documentation](https://www.tensorflow.org/)
- [Pygame Documentation](https://www.pygame.org/docs/)
