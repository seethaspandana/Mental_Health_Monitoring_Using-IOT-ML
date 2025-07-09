🧠 Mental Health Monitoring System using IoT & Machine Learning

This project presents a smart **Mental Health Monitoring System** that integrates **IoT sensors** and **Machine Learning algorithms** to track and assess the mental well-being of users in real time.

Wearable sensors capture physiological signals such as:
- 🌡️ Temperature (via DHT11)
- ❤️ Pulse Rate (via Pulse Sensor)
- 💧 Galvanic Skin Response - GSR (for stress detection)
- 🌀 Head Tilt Detection (via MPU6050)

Data is transmitted through an ESP32 to **Firebase** and visualized on a **Flask Web Dashboard** with suggestions based on ML predictions.

📌 Features
- Real-time monitoring of multiple physiological parameters
- Machine Learning-based stress classification (Random Forest Classifier)
- User-friendly dashboard with:
  - Live charts (Chart.js)
  - Mood-based suggestions
  - Patient-wise records
- Voice alerts for abnormal conditions
- Firebase integration for live data storage and retrieval

 🛠️ Technologies Used
- Hardware: ESP32, DHT11, Pulse Sensor, GSR Sensor, MPU6050
- Backend: Python, Flask, Firebase
- Frontend: HTML, CSS, Chart.js
- Machine Learning: Scikit-learn (Random Forest Classifier)
- Database: Firebase Realtime Database

 📁 Folder Structure
Mental Health Monitoring project/
│
├── ML\_Model/              # Jupyter notebooks, trained ML model (.pkl)
├── Web\_Dashboard/         # Flask app with templates and static files
├── ESP32\_Code/            # Arduino code for ESP32 + sensor integration
├── Presentation/          # PPT and report files
├── Documentation/         # Abstract, project report
└── README.md              # Project readme file

🚀 Setup Instructions

### 1. Clone the Repository
bash
git clone https://github.com/Kasturi3004/Mental-Health-Monitoring.git
cd Mental-Health-Monitoring

### 2. Configure Firebase
* Set up a Firebase Realtime Database project.
* Replace Firebase credentials in the Flask app (`firebase_config` in `Web_Dashboard/app.py`).

### 3. Run Flask Web App
bash
cd Web_Dashboard
pip install -r requirements.txt
python app.py

Access the dashboard at `http://localhost:5000`

4. Upload Firmware to ESP32
* Use Arduino IDE.
* Install required libraries for DHT, MPU6050, and Firebase.
* Upload `ESP32_Code/mental_health_monitor.ino`.

📊 Machine Learning
* Model: Random Forest Classifier
* Input Features: Pulse, Temperature, GSR
* Output Labels: Normal, Stressed, Calm
* Accuracy: \~100%
* Validation Accuracy: \~99.5%
* Training done on simulated + collected data

🎯 Use Cases
* Student wellness monitoring
* Factory worker stress detection
* Driver alertness system
* Personal health assistant

📚 Documentation
*  PPT Presentation
*  Detailed Project Report
*  Source Code & Dataset
*  Deployment Guide

🙌 Acknowledgements
* Firebase by Google
* Chart.js for visualization
* Scikit-learn for ML
* IoT sensor libraries & open community
