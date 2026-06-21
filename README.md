# 🎙️ Speech Recognition and Emotion Detection

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-CNN-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-Deployed-red)
![MFCC](https://img.shields.io/badge/Feature-MFCC-yellow)
![Deep Learning](https://img.shields.io/badge/AI-DeepLearning-green)
![CVIP 2025](https://img.shields.io/badge/Research-CVIP2025-purple)
![XAI](https://img.shields.io/badge/Explainability-LMAC-success)

A real-time **Speech Emotion Recognition (SER)** system that analyzes human speech and predicts emotional states using deep learning, while also providing interpretable explanations of model decisions.

This project combines **speech processing**, **deep learning**, and **Explainable AI (XAI)** to understand not just *what emotion is being spoken*, but also *why the model predicted it*.

The system extracts speech features like **MFCCs, Chroma, Mel Spectrograms, Spectral Contrast, Tonnetz, Pitch, and Energy**, and uses a **CNN-GRU-Attention** based architecture for emotion classification.

The project also integrates **Local Model-Agnostic Classification (LMAC)** for post-hoc interpretability, making the predictions more transparent and trustworthy.

This work was developed as my final-year undergraduate research project at **National Institute of Technology Calicut** and was accepted at **CVIP 2025 (IIT Ropar)**.

---

## 🚀 Why This Project?

Speech carries more than words — it carries emotions.

Traditional speech recognition systems focus on *what is being said*, but emotional intelligence in AI requires understanding *how it is being said*.

This project aims to bridge that gap by making speech systems:

* More emotionally aware
* More interpretable
* More trustworthy
* More suitable for real-world human-centric AI applications

Applications include:

* Virtual Assistants
* Mental Health Monitoring
* Customer Support Analytics
* Human-Computer Interaction
* Emotion-Aware Chatbots
* Smart Call Center Systems

---

## ✨ Features

✔️ Real-time Speech Emotion Recognition
✔️ CNN-GRU-Attention based architecture
✔️ Advanced speech feature extraction
✔️ Explainable AI using LMAC
✔️ Interactive Streamlit web application
✔️ Upload custom audio files
✔️ Waveform visualization
✔️ Spectrogram visualization
✔️ Emotion prediction with interpretability

---

## 🧠 Model Architecture

The emotion detection pipeline follows:

```text
Audio Input
   ↓
Preprocessing
   ↓
Feature Extraction
(MFCC + Chroma + Mel + Tonnetz + Contrast + Pitch + Energy)
   ↓
CNN Layers
   ↓
Bi-Directional GRU
   ↓
Attention Layer
   ↓
Dense Layers
   ↓
Softmax Classification
   ↓
Emotion Prediction
   ↓
LMAC Explainability
```

---

## 🎯 Emotion Classes

The model classifies speech into:

* Angry
* Disgust
* Fear
* Happy
* Neutral
* Sad
* Sarcastic
* Surprise

---

## 🛠️ Tech Stack

### Programming & Frameworks

* Python
* TensorFlow
* Streamlit

### Audio Processing

* Librosa
* NumPy
* Pandas

### Machine Learning

* Scikit-learn
* StandardScaler
* LabelEncoder

### Deep Learning

* CNN
* Bi-directional GRU
* Attention Mechanism

### Explainability

* Local Model-Agnostic Classification (LMAC)

---

## 📂 Project Structure

```bash
emotion-app/
│── model/                    # Trained model files
│── screenshots/              # Visual outputs
│── dataset/                  # Audio datasets
│── app.py                    # Streamlit application
│── train_model.py            # Training pipeline
│── requirements.txt          # Dependencies
│── README.md                 # Documentation
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

### Prediction Output

Shows the predicted emotion from the uploaded speech sample.

![Prediction Output](screenshots/prediction_output.png)

---

### Spectrogram Visualization

Displays time-frequency representation of speech.

![Spectrogram](screenshots/spectrogram.png)

---

### Waveform Visualization

Shows amplitude variation over time.

![Waveform](screenshots/waveform.png)

---

## 📊 Model Performance

The model was trained on a combination of a custom dataset (**BhavanaVani**) and a public Hindi SER dataset.

### Performance Metrics

* **Training Accuracy:** 99.71%
* **Validation Accuracy:** 72.34%
* **Overall Test Accuracy:** 72.34%

### Class-wise F1 Scores

* Anger → **83.1%**
* Fear → **77.7%**
* Sad → **73.2%**
* Surprise → **71.3%**
* Neutral → **68.0%**
* Happy → **65.3%**
* Disgust → **64.1%**
* Sarcastic → **60.8%**

---

## 🔍 Explainability Metrics (LMAC)

To improve transparency, the model uses **LMAC** to identify important speech segments contributing to predictions.

### Interpretability Performance

* **Mask-In L2I Score:** 0.91
* **Mask-Out L2I Score:** 0.83
* **Structural AUC:** 0.88
* **Average Gain:** 12.7%
* **Average Drop:** 8.1%
* **Sparseness:** 61.4%
* **Complexity Index:** 0.37

These metrics indicate strong faithfulness and high-quality interpretability.

---

## 🔬 Research Contribution

This project contributed to the research paper:

**SPASHTA — Speech Posthoc Attribution with Salient Highlighting for Transparent Analysis**

Accepted at:

**Conference on Computer Vision and Image Processing (CVIP 2025), IIT Ropar**

### Key Contributions:

* Built the **BhavanaVani** custom Hindi speech dataset
* Developed a CNN-GRU-Attention based SER pipeline
* Implemented post-hoc explainability using LMAC
* Evaluated model faithfulness using structural metrics
* Improved transparency in low-resource speech systems
* Validated explanations using human and empirical analysis

---

## 📝 Peer Review Highlights

The work received positive peer-review feedback for:

* Novelty in Explainable AI for Speech Emotion Recognition
* Human-understandable listenable explanations
* Applicability in low-resource Indic language settings
* Strong interpretability framework

---

## 🔮 Future Improvements

* Real-time microphone support
* Transformer-based architectures (Wav2Vec2, HuBERT, Whisper)
* Multilingual emotion recognition
* Model compression for mobile deployment
* Noise-robust emotion classification
* Multimodal emotion recognition (audio + video + text)
* Emotion trajectory tracking

---

## 👨‍💻 Author

**Saurav Kumar Singh**
B.Tech CSE | National Institute of Technology Calicut
AI/ML Engineer | Speech AI | Deep Learning | Explainable AI

GitHub: https://github.com/build-with-saurav

---

## 📜 License

This project is intended for educational and research purposes only.
