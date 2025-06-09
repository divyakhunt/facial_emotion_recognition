# 😄 Facial Emotion Recognition with ResNet50

This project performs facial emotion recognition using a deep learning approach with TensorFlow and a pretrained ResNet50 model. It uses the FER (Facial Emotion Recognition) dataset available on Kaggle and processes grayscale images to classify human emotions.

---

## 📁 Dataset

- **Dataset**: [Emotion Detection FER](https://www.kaggle.com/datasets/ananthu017/emotion-detection-fer)
- **Source**: Kaggle
- **Structure**:
  - The dataset is organized into training and test directories, each containing emotion-based subfolders (e.g., happy, sad, angry, disgusted, etc.).
  - Images are in **grayscale**, and converted to **RGB** for model compatibility.

---

## 🧠 Model Architecture

- **Base Model**: Pretrained `ResNet50` (ImageNet weights, excluding top layer)
- **Custom Head**:
  - Global Average Pooling
  - Dense layer with 256 units (ReLU)
  - Output layer with Softmax activation for emotion classification

---

## 🔧 Preprocessing & Augmentation

- Convert grayscale images to RGB
- Normalize pixel values to [0, 1]
- Augment training data with:
  - Rotation
  - Zoom
  - Horizontal Flip
  - Shearing
  - Width and Hight shifting

---

## 🏗️ Training Setup

- **Framework**: TensorFlow / Keras
- **Input Size**: 224x224
- **Batch Size**: 64
- **Loss**: Sparse Categorical Crossentropy
- **Optimizer**: Adam
- **Callbacks**:
  - EarlyStopping (patience=7)

---

## 📊 Performance Tracking

- Training and validation accuracy/loss plotted over epochs
- Confusion matrix to analyze class-wise prediction performance

---

## 📦 Installation & Running

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/facial_emotion_recognition.git
   cd facial_emotion_recognition
   ```

2. Install requirements:
   ```bash
   pip install -r requirements.txt
   ```

3. Set up your Kaggle API key (`kaggle.json`) and run the notebook:
   ```bash
   # Place kaggle.json in root or ~/.kaggle/
   jupyter notebook facial_emotion_recognition.ipynb
   ```

---

## 🙋‍♂️ Emotions Covered

- Angry 😠
- Disgusted 🤢
- Fearful 😨
- Happy 😄
- Neutral 😐
- Sad 😢
- Surprised 😮

---

## 📌 Future Improvements

- Add GUI using Streamlit or Gradio
- Deploy as a web application
- Explore EfficientNet or Vision Transformers for accuracy boost

---

## 📜 License

This project is under the MIT License.
