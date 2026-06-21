# 🎙️ Speech Recognition and Emotion Detection

![Python](https://img.shields.io/badge/Python-3.10-blue)
![TensorFlow](https://img.shields.io/badge/TensorFlow-CNN-orange)
![Streamlit](https://img.shields.io/badge/Streamlit-Deployed-red)
![MFCC](https://img.shields.io/badge/Feature-MFCC-yellow)
![Deep Learning](https://img.shields.io/badge/AI-DeepLearning-green)
![CVIP 2025](https://img.shields.io/badge/Research-CVIP2025-purple)
![XAI](https://img.shields.io/badge/Explainability-LMAC-success)

A real-time **Speech Emotion Recognition (SER)** system that analyzes human speech and predicts emotional states using deep learning while also providing interpretable explanations of model decisions.

This project combines **speech processing**, **deep learning**, and **Explainable AI (XAI)** to understand not just *what emotion is being spoken*, but also *why the model predicted it*.

The system extracts speech features such as **MFCCs, Chroma, Mel Spectrograms, Spectral Contrast, Tonnetz, Pitch, and Energy**, and uses a **CNN-GRU-Attention** architecture for emotion classification.

To improve transparency, the system integrates **Local Model-Agnostic Classification (LMAC)** for post-hoc interpretability.

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

### Applications

* Virtual Assistants
* Mental Health Monitoring
* Customer Support Analytics
* Human-Computer Interaction
* Emotion-Aware Chatbots
* Smart Call Center Systems

---

## ✨ Features

* Real-time Speech Emotion Recognition
* CNN-GRU-Attention based architecture
* Advanced speech feature extraction
* Explainable AI using LMAC
* Interactive Streamlit web application
* Upload custom audio files
* Waveform visualization
* Spectrogram visualization
* Emotion prediction with interpretability

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

## 📁 Dataset Information

This project follows a **two-stage hybrid dataset approach**.

### 1. BhavanaVani (Custom Dataset)

BhavanaVani is a custom Hindi emotional speech dataset initiated during this project.

We initially collected emotion-labeled speech samples from students at **National Institute of Technology Calicut**.

Challenges faced:

* Limited participation
* Class imbalance
* Low sample count
* Difficulty in collecting natural emotional speech

This dataset helped establish the initial training pipeline.

---

### 2. Kaggle Hindi SER Dataset

To overcome data limitations, we incorporated a larger Hindi Speech Emotion Recognition dataset from Kaggle.

This helped improve:

* Dataset diversity
* Better class balance
* Improved generalization
* Stronger model robustness

Final hybrid dataset size: **3200+ audio samples**

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
* Bi-Directional GRU
* Attention Mechanism

### Explainability

* Local Model-Agnostic Classification (LMAC)

---

## 📂 Project Structure

```bash
emotion-app/
│── model/                     # Trained model files
│── script/                    # Training and preprocessing scripts
│── screenshots/               # Visual outputs
│── README.md                  # Documentation
│── requirements.txt           # Dependencies
│── emotions.csv               # Emotion labels
│── confusion_matrix_eval.png  # BhavanaVani evaluation
```

---

## ⚙️ Installation & Setup

### 1. Clone the repository

```bash
git clone https://github.com/build-with-saurav/emotion-app.git
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

Shows the predicted emotion from uploaded speech.

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

The model was trained using a **hybrid dataset strategy**.

### Phase 1 — BhavanaVani (Custom Dataset)

The initial model was trained using the custom BhavanaVani dataset collected from NIT Calicut students.

This phase helped validate:

* Feature extraction pipeline
* Emotion labeling consistency
* Initial model architecture

### BhavanaVani Confusion Matrix

![BhavanaVani Confusion Matrix](confusion_matrix_eval.png)

---

### Phase 2 — Kaggle Hindi SER Dataset

To improve robustness and scale, we extended training using a Kaggle Hindi SER dataset.

### Final Performance Metrics

* **Training Accuracy:** 99.71%
* **Validation Accuracy:** 72.34%
* **Overall Confusion Matrix Accuracy:** 94.59%


### Kaggle Dataset Confusion Matrix

The confusion matrix below shows the final classification performance after extending training with the larger Kaggle Hindi SER dataset.

This experiment improved robustness, class balance, and generalization across all emotion categories.

![Kaggle Confusion Matrix](screenshots/kaggle_confusion_matrix.png)

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

These metrics demonstrate strong faithfulness and high-quality interpretability.

---

## 🔬 Research Contribution

This project contributed to the research paper:

**SPASHTA — Speech Posthoc Attribution with Salient Highlighting for Transparent Analysis**

Accepted at:

**Conference on Computer Vision and Image Processing (CVIP 2025), IIT Ropar**

### Key Contributions

* Initiated custom Hindi speech dataset collection from NIT Calicut students
* Designed the speech data collection pipeline
* Identified dataset limitations and expanded with Kaggle data
* Built a hybrid dataset for improved generalization
* Developed CNN-GRU-Attention based SER pipeline
* Implemented post-hoc explainability using LMAC
* Evaluated model faithfulness using structural metrics
* Improved transparency in low-resource Indic speech systems
* Validated explanations using empirical and human analysis

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
