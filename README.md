***

# 🎛️ Gesture Volume Control Using Hand Gestures 🤚🔊

Control your computer’s **audio volume in real-time** using natural hand gestures detected through your webcam! This Python project utilizes cutting-edge technologies to create an intuitive, touchless volume controller.

***

## 🚀 Features

- 🤖 **Real-time Hand Tracking** with MediaPipe’s state-of-the-art hand landmark model  
- ✋ Detects thumb and index finger tip positions to interpret volume gestures  
- 🎚️ Maps finger distance dynamically to system volume using Pycaw  
- 📊 Visual feedback via landmark drawings, connecting lines, and a live volume bar overlay  
- 💻 Compatible with Windows OS (leverages Windows Core Audio API)  

***

## 🛠️ Prerequisites

- Python 3.7+  
- Webcam compatible with OpenCV  
- Windows system (for Pycaw audio control)  

***

## 🧩 Installation

1. Clone the repository to your local machine.  
2. Install dependencies quickly with the `requirements.txt`:  

```bash
pip install -r requirements.txt
```

`requirements.txt` includes:  
```
opencv-python
mediapipe
numpy
comtypes
pycaw
```

***

## 🎬 How to Use

Run the script:

```bash
python main.py
```

- Position your hand in front of the webcam 🤳  
- Pinch your thumb and index finger to adjust the volume:  
   - 🤏 Closer fingers = decrease volume  
   - ✋ Spread fingers = increase volume  
- The connecting line turns **red 🔴** when fingers are very close  
- Volume percentage and bar show real-time audio level feedback  
- Press **q** to quit  

***

## ⚙️ How It Works

- The webcam feed captures live video frames via OpenCV 📹  
- MediaPipe processes frames to detect and track multiple hand landmarks 🤖  
- Coordinates of thumb tip (landmark 4) and index finger tip (landmark 8) are extracted ✨  
- Calculates Euclidean distance between these fingertips 🔢  
- Distance is interpolated to the system’s volume range supported by Windows 🖥️  
- Pycaw sets master volume level programmatically based on gesture input 🔊  

***

## 🔍 Code Highlights

- `cv2` for real-time video processing and GUI rendering  
- `mediapipe` for accurate and efficient hand landmark detection  
- `numpy` and `math` for numerical computations  
- `pycaw` for interfacing with Windows Core Audio API to control audio volume  

***

## 💡 Additional Notes

- Volume control is calibrated between finger distances of 50 to 220 pixels  
- Visual cues enhance user feedback for seamless interaction 🚦  
- Ensure your webcam permissions are enabled for smooth operation  

***

📜 License
This project is licensed under the MIT License © 2025 Praneeth N.

See the [LICENSE](LICENSE) file for details.



***

Enjoy a futuristic, **touchless audio control experience** powered by AI and computer vision! 🤖✨🔊

***

This version adds a technological vibe with emojis and highlights the advanced tech involved for an engaging and clear project introduction.

***
