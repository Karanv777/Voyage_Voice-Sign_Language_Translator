# Voyage Voice

**Voyage Voice** is a real-time Sign Language-to-Text translation system that bridges the communication gap for the hearing and speech-impaired. Using Computer Vision and Deep Learning, the application captures hand landmarks and translates gestures into meaningful text and speech in real-time.

🔗 **Live App:** [voyage-voice.streamlit.app](https://voyage-voice.streamlit.app/)

🔗 **GitHub Repository:** [Karanv777/Sign_Language_Translator](https://github.com/Karanv777/Sign_Language_Translator)

---

## 🌟 Key Features

* **Real-time Detection:** High-speed hand gesture recognition using your webcam.
* **Neural Network Powered:** Uses a custom-trained CNN (Convolutional Neural Network) to classify hand landmarks.
* **Mediapipe Integration:** Leverages Google's Mediapipe for robust and accurate 21-point hand landmark tracking.
* **Text-to-Speech (TTS):** Converts translated text into audible speech for seamless communication.

---

## 🛠️ Tech Stack

* **Frontend:** [Streamlit](https://streamlit.io/) (for the web interface)
* **Computer Vision:** [OpenCV](https://opencv.org/), [MediaPipe](https://www.google.com/search?q=https://google.github.io/mediapipe/)
* **Deep Learning:** [PyTorch](https://pytorch.org/) / [TensorFlow](https://www.tensorflow.org/)
* **Programming Language:** Python 3.10
* **Deployment:** Streamlit Cloud

---

## 🚀 How It Works

1. **Landmark Extraction:** The application captures video frames and uses MediaPipe to extract  coordinates for 21 hand landmarks.
2. **Feature Engineering:** Coordinates are normalized relative to the bounding box of the hand to ensure the model is scale-invariant.
3. **Inference:** These features are fed into a pre-trained Deep Learning model (`asl1.pth`).
4. **Output:** The model predicts the gesture (e.g., American Sign Language alphabets), displays it on the screen.

---

## 💻 Local Installation

To run this project on your local machine, follow these steps:

### 1. Clone the repository

```bash
git clone https://github.com/Karanv777/Sign_Language_Translator.git
cd Sign_Language_Translator

```

### 2. Create a Virtual Environment (Optional but recommended)

```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate

```

### 3. Install Dependencies

```bash
pip install -r requirements.txt

```

### 4. Run the Application

```bash
streamlit run app.py

```

---

## 📂 Project Structure

```text
├── data/               # Dataset used for training labels
├── asl1.pth            # Saved model weights
├── app.py              # Main Streamlit application
├── letters/            # letters in the Sign Language
├── requirements.txt    # List of required Python packages
└── README.md           # Project documentation

```

---

## 🤝 Contributing

Contributions are welcome! If you have ideas for improving the accuracy, adding more gestures, or enhancing the UI.
