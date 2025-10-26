AUTISM PREDICTION USING DEEP LEARNING

This project uses deep learning techniques to automatically detect Autism Spectrum Disorder (ASD) traits from short video clips.
It combines Convolutional Neural Networks (CNNs) and Long Short-Term Memory (LSTM) layers to extract both spatial and temporal behavioral cues such as facial expressions, gaze patterns, and movements.

 📁 Project Structure

Autism-Detection-Video/
│
├── newdataset/
│   ├── autismdataset/          # Videos labeled as Autism (1)
│   └── nonautismdataset/       # Videos labeled as Non-Autism (0)
│
├── video_autism_detection.py   # Main training + testing code
├── video_autism_model.h5       # Saved trained model
├── README.txt                  # Project documentation
└── requirements.txt            # Python dependencies

🚀 Features

✅ Automatic extraction of key video frames
✅ CNN for spatial feature extraction
✅ LSTM for temporal sequence learning
✅ Binary classification: Autism / Non-Autism
✅ Real-time prediction with OpenCV video display

🧩 Model Architecture

The model uses a TimeDistributed CNN + LSTM hybrid design:

1. CNN Layers — extract spatial features (facial cues, movements)
2. MaxPooling — reduce dimensionality
3. Flatten + LSTM Layer — capture sequential dependencies between frames
4. Dense Layers — classify between Autism and Non-Autism

⚙️ Installation

1️⃣ Clone the Repository
> git clone https://github.com/yourusername/Autism-Detection-Video.git
> cd Autism-Detection-Video

2️⃣ Install Dependencies
> pip install -r requirements.txt

Or manually install:
> pip install tensorflow numpy opencv-python scikit-learn

🧾 Usage

Ensure dataset folders are structured as:

newdataset/
├── autismdataset/
│   ├── video1.mp4
│   └── video2.mp4
└── nonautismdataset/
    ├── videoA.mp4
    └── videoB.mp4

Run the model:
> python video\_autism\_detection.py

🎥 Prediction

> video\_path = r"path\_to\_your\_video.mp4"
> predict\_and\_show(video\_path)

Press ‘q’ to close the OpenCV video window.

📊 Evaluation

Loss Function: Binary Crossentropy
Optimizer: Adam
Metrics: Accuracy
Validation Split: 20%
Epochs: 10
Batch Size: 4

🧪 Example Output

Dataset shape: (120, 20, 64, 64, 3) (120,)
Epoch 10/10
Validation Accuracy: 92.5%
Test Accuracy: 91.8%
Prediction: Autism (Confidence: 0.87)

🧑‍💻 Technologies Used

Python 3.9+
TensorFlow / Keras
OpenCV
NumPy
Scikit-learn