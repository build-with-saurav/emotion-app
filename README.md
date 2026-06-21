# 🎙️ Speech Recognition and Emotion Detection

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-CNN-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-Deployed-red)
![MFCC](https://img.shields.io/badge/Feature-MFCC-yellow)
![Deep Learning](https://img.shields.io/badge/AI-DeepLearning-green)
![CVIP 2025](https://img.shields.io/badge/Research-CVIP2025-purple)

A real-time **Speech Emotion Recognition (SER)** system that analyzes human speech and predicts emotional states using deep learning.

This project focuses on understanding the emotional context behind spoken language by extracting **MFCC (Mel-Frequency Cepstral Coefficients)** from audio signals and feeding them into a **Convolutional Neural Network (CNN)** for classification.

The system is deployed using **Streamlit**, providing a clean and interactive web interface where users can upload audio files and receive instant emotion predictions.

This work was developed as my final-year research project and was accepted at **CVIP 2025 (IIT Ropar)**.

---

## 🚀 Why This Project?

Speech carries more than words — it carries emotions. Traditional speech recognition systems focus only on *what is being said*, but not *how it is being said*.

This project helps bridge that gap by enabling machines to understand emotional context from speech, making it useful for:

* Virtual Assistants
* Mental Health Monitoring
* Customer Support Analytics
* Human-Computer Interaction
* Smart Call Center Systems

---

## ✨ Features

✔️ Detect emotions from speech/audio input
✔️ Deep learning-based CNN model
✔️ MFCC feature extraction
✔️ Streamlit-powered web application
✔️ Upload custom audio files for prediction
✔️ Fast and accurate inference
✔️ User-friendly interface

---

## 🧠 Model Architecture

The emotion detection pipeline follows:

```text
Audio Input
   ↓
Preprocessing
   ↓
MFCC Feature Extraction
   ↓
CNN Layers
   ↓
Dense Layers
   ↓
Softmax Classification
   ↓
Emotion Prediction
```

---

## 🎯 Emotion Classes

The model classifies speech into:

* Angry
* Calm
* Happy
* Sad
* Fearful
* Disgust
* Neutral

---

## 🛠️ Tech Stack

### Programming & Frameworks

* Python
* TensorFlow
* Streamlit

### Audio Processing

* Librosa
* NumPy

### Deep Learning

* Convolutional Neural Network (CNN)
* MFCC Feature Engineering

---

## 📂 Project Structure

```bash
emotion-app/
│── model/                 # Trained CNN model
│── screenshots/           # Application screenshots
│── app.py                 # Streamlit web application
│── requirements.txt       # Dependencies
│── README.md              # Project documentation
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/SauravB210489CS/emotion-app.git
cd emotion-app
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the application

```bash
streamlit run app.py
```

---

## 📸 Application Screenshots

### Home Page

![Home](screenshots/home.png)

### Upload Audio Interface

![Upload](screenshots/upload.png)

### Prediction Results

![Results](screenshots/result.png)

---

## 📊 Model Details

* CNN-based architecture for speech emotion recognition
* MFCC feature extraction for robust audio representation
* Trained on labeled emotional speech datasets
* Optimized using TensorFlow
* Designed for real-time inference
* High prediction performance

---

## 🔬 Research Contribution

This project was developed as part of my undergraduate final-year research work and contributed to my accepted paper at:

**Conference on Computer Vision and Image Processing (CVIP 2025), IIT Ropar**

### Key Contributions:

* Built the complete speech preprocessing pipeline
* Implemented MFCC-based feature extraction
* Designed and trained CNN architecture
* Developed real-time deployment using Streamlit
* Improved speech emotion classification performance

---

## 🔮 Future Improvements

* Real-time microphone input
* Noise reduction pipeline
* Transformer-based speech models
* Multi-language emotion recognition
* Improved accuracy with larger datasets
* Integration with speech-to-text systems

---

## 👨‍💻 Author

**Saurav Kumar Singh**
B.Tech CSE | National Institute of Technology Calicut
AI/ML Engineer | Speech AI | Deep Learning

GitHub: https://github.com/build-with-saurav

---

## 📜 License

This project is intended for educational and research purposes only.
