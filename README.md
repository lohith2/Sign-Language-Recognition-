# 🤟 Sign Language Recognition using CNN & OpenCV

A deep learning–based **real-time Sign Language Recognition System** that uses **Convolutional Neural Networks (CNNs)** and **OpenCV** to detect and classify hand gestures into sign language letters or words.  

This project allows users to train their own models, capture gesture datasets, and perform live recognition via webcam.

---

## 🧠 Features

- 🖐️ Real-time **hand gesture recognition** using webcam  
- 🧩 **CNN model** trained on image datasets for sign language alphabets  
- 🧰 Modular design with separate scripts for **data capture**, **training**, and **testing**  
- 📊 Supports model evaluation and accuracy visualization  
- ⚡ Fast and lightweight implementation using **OpenCV**, **TensorFlow/Keras**, and **NumPy**

---

## 🏗️ Project Structure

```
Sign-Language-Recognition--main/
│
├── Capture.py          # Capture sign images from webcam and store them for dataset creation
├── cnn.py              # Define, train, and save CNN model for gesture recognition
├── recognize.py        # Real-time recognition using trained CNN model + webcam feed
├── test.py             # Evaluate the model performance on test data
└── README.md           # Project documentation
```

---

## ⚙️ Requirements

Install dependencies:

```bash
pip install opencv-python tensorflow keras numpy matplotlib
```

---

## 🚀 How to Use

### 1️⃣ Capture Training Data

Run the capture script to collect images of different gestures for training:

```bash
python Capture.py
```

This will open your webcam and allow you to capture sign images (one per class).  
Images are saved in corresponding folders for dataset preparation.

---

### 2️⃣ Train the CNN Model

Train the model on your dataset:

```bash
python cnn.py
```

The script will:
- Load and preprocess training images  
- Define a **Convolutional Neural Network**  
- Train and save the model as `model.h5`  

---

### 3️⃣ Test the Model

Evaluate accuracy on the test dataset:

```bash
python test.py
```

You’ll see model accuracy and loss visualizations.

---

### 4️⃣ Real-Time Sign Recognition

Run live recognition through webcam:

```bash
python recognize.py
```

The model predicts the sign shown in front of your camera in real-time.

---

## 🧩 CNN Model Architecture (Example)

| Layer | Type | Output Shape |
|-------|------|---------------|
| 1 | Conv2D (32 filters, 3x3) | (64, 64, 32) |
| 2 | MaxPooling2D | (32, 32, 32) |
| 3 | Conv2D (64 filters, 3x3) | (32, 32, 64) |
| 4 | MaxPooling2D | (16, 16, 64) |
| 5 | Flatten | - |
| 6 | Dense (128, relu) | 128 |
| 7 | Dense (output, softmax) | num_classes |

---

## 🧾 Dataset

You can use:
- A **custom dataset** created using `Capture.py`, or  
- Public datasets such as:
  - [Sign Language MNIST](https://www.kaggle.com/datamunge/sign-language-mnist)  
  - [ASL Alphabet Dataset](https://www.kaggle.com/grassknoted/asl-alphabet)

---

## 🧪 Example Output

- Camera window displays **live video feed**  
- Predicted letter/word is shown on-screen in real-time  
- Confidence level (probability) may also be printed in the console

---

