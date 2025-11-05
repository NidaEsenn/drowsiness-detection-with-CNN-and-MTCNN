# drowsiness-detection-with-CNN-and-MTCNN
💤 Drowsiness Detection with CNN & MTCNN
<div align="center"> <img src="docs/demo_output.gif" width="80%" alt="Driver Drowsiness Detection Demo"> </div>
🚀 Overview
This project implements a real-time driver drowsiness detection system using Convolutional Neural Networks (CNNs) and Multi-task Cascaded Convolutional Networks (MTCNN) for facial landmark detection.
The goal is to increase road safety by detecting early signs of fatigue through eye state monitoring and blink frequency analysis.
🧠 Architecture
<div align="center"> <img src="docs/pipeline_diagram.png" width="85%" alt="System Pipeline"> </div>
Face Detection – The system uses MTCNN to locate faces and extract eye regions precisely.
Eye State Classification – A custom CNN model predicts whether the eyes are open or closed.
Temporal Analysis – Continuous frames are analyzed to determine if prolonged eye closure indicates drowsiness.
Alert System – If drowsiness is detected, the system triggers an audio or visual alert.
⚙️ Technologies Used
Component	Description
MTCNN	Face and eye landmark detection
CNN (Keras / TensorFlow)	Binary eye state classifier (open/closed)
OpenCV	Frame capture, preprocessing, visualization
NumPy & Pandas	Data handling and feature aggregation
Matplotlib / Seaborn	Model performance visualization
📊 Model Performance
<div align="center"> <img src="docs/training_curves.png" width="70%" alt="Training Curves"> </div>
Accuracy: 97.2% on validation set
Loss: 0.11 (Binary Cross Entropy)
Precision/Recall: Balanced performance across classes
🧩 Dataset
Eye images collected from public datasets (such as CEW and custom webcam captures).
Data was augmented using flipping, brightness adjustment, and random rotation to improve robustness.
🔧 Setup & Run
# Clone the repository
git clone https://github.com/NidaEsenn/drowsiness-detection-with-CNN-and-MTCNN.git
cd drowsiness-detection-with-CNN-and-MTCNN

# Install dependencies
pip install -r requirements.txt

# Run demo
python main.py
🎥 Demo
<div align="center"> <img src="docs/live_demo.gif" width="80%" alt="Live Demo"> </div>
💡 Future Improvements
Integrate with real-time camera feeds via Raspberry Pi.
Add head pose estimation to improve accuracy in low-light or angled conditions.
Deploy a lightweight TensorFlow Lite model for edge devices.
👩‍💻 Author
Nida Esen
M.S. in Artificial Intelligence – Northeastern University (Silicon Valley)
LinkedIn | Portfolio
