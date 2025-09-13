# Drowsiness Detection System 🚗💤

This project detects driver drowsiness using real-time grayscale video input. It monitors eye states using Haar cascades and a trained CNN model, triggering an alarm when prolonged eye closure is detected. The system resets when the driver regains focus.

## 📸 Features
- Real-time webcam feed analysis
- Grayscale image processing for performance
- Eye state classification using CNN
- Alarm system triggered at drowsiness threshold
- Auto-reset when driver is alert

## 🛠️ Tech Stack
- Python
- OpenCV
- Keras (TensorFlow backend)
- Pygame (for alarm sound)
- Haar Cascade Classifiers

## 📁 Project Structure
```
DROWSINESS_detection/ 
├── haar_cascade_files/ 
│ ├── haarcascade_frontalface_alt.xml 
│ ├── haarcascade_lefteye_2splits.xml 
│ └── haarcascade_righteye_2splits.xml 
├── models/ 
│ └── cnnCat2.h5 
├── assets/ 
│ └── alarm.wav 
├── src/ 
│ ├── drowsiness_detection.py 
│ └── model.py 
├── demo/ 
│ └── image.jpg 
├── requirements.txt 
├── .gitignore 
├── config.py
└── README.md
```


## 🚀 Getting Started

### 1. Clone the Repository
```bash
git clone https://github.com/your-username/drowsiness-detection-system.git
cd drowsiness-detection-system
```

### 2. Set Up Environment
Create a virtual environment (optional but recommended):

```bash
python -m venv env
source env/bin/activate  # On Windows: env\Scripts\activate
```
### 3. Install Dependencies
```bash
pip install -r requirements.txt
```
### 4. Run the Detection Script
```bash
python src/drowsiness_detection.py
```

## 🎯 How It Works
Haar cascades detect face and eyes.

CNN model classifies eye state (Open/Closed).

Score increments with closed eyes.

Alarm triggers when score ≥ 25.

Score drops by 3 when eyes reopen and focus is regained.

## 📌 Notes
Ensure webcam access is granted.

Place alarm.wav and cnnCat2.h5 in correct paths.

Works best in well-lit conditions.
