# TuberDetect: AI-Powered Tuberculosis Detection from Chest X-rays
TuberDetect is a deep learning project designed to detect signs of tuberculosis (TB) from chest X-ray images using a Convolutional Neural Network (CNN). This model classifies images into two categories: Tuberculosis and Normal.

📂 Project Structure

TuberDetect/
├── data/
│   ├── Normal/
│   ├── Tuberculosis/
│   ├── Normal.metadata.xlsx
│   └── Tuberculosis.metadata.xlsx
├── model/
│   └── my_model.hdf5
├── notebook/
│   └── TuberDetect_Demo.ipynb
└── README.md

🧠 Model Architecture
3 Convolutional layers with MaxPooling

Flatten layer followed by multiple Dense layers

Dropout regularization to prevent overfitting

Final layer with 2 output neurons for binary classification

The model was trained on preprocessed grayscale images resized to 28x28 to keep it lightweight and interpretable.

✅ Features
CNN-based classifier trained on real X-ray images

Handles both .png and .jpeg inputs

Mounted Google Drive integration for easy data handling

Visualization of predictions with image overlays


# Web Interface

![6](https://user-images.githubusercontent.com/105975325/201843423-0c24a9bd-c9ac-47f2-956d-e3c2418b3d23.png)

# output
![7](https://user-images.githubusercontent.com/105975325/201843445-5b371a36-e552-48a7-9b1b-9a5eeddf8831.png)
![8](https://user-images.githubusercontent.com/105975325/201843450-6fb37311-be6d-4503-a6a9-2bde0bdce3f8.png) 


🚀 How to Run
Mount Google Drive:

from google.colab import drive
drive.mount('/content/drive')

Clone the repo and open notebook:

!git clone https://github.com/yourusername/TuberDetect.git
Run TuberDetect_Demo.ipynb inside the notebook/ folder.

🔍 Example Prediction Code

image = preprocess_image('/path/to/image.png')
prediction = model.predict(image)
label = "Tuberculosis" if prediction[0][0] > 0.5 else "Normal"

📊 Dataset
This project uses a subset of publicly available X-ray images labeled as:
Normal
Tuberculosis

Each image is accompanied by metadata (resolution, size, format, etc.).

🛠️ Tech Stack
Python
TensorFlow / Keras
OpenCV
Google Colab
Matplotlib / NumPy / Pandas

🙌 Credits
Made by Anagha as part of an AI-driven healthcare initiative.
