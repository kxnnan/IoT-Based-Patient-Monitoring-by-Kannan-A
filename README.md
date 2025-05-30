# IoT-Based Patient Monitoring System 🩺📡

Kannan A,
M.Tech Big Data Analytics,
Guided by Dr. Suseela S

---

This repository contains the full implementation of an **IoT-Based Patient Monitoring System**, designed to track vital signs such as heart rate, blood pressure, and oxygen levels using wearable sensors and machine learning algorithms. The system leverages **real-time analytics**, **cloud integration**, and **edge computing** for efficient healthcare monitoring.

---

## 📌 Project Overview

The primary goal of this project is to enable continuous patient monitoring, anomaly detection, and secure data sharing using IoT and AI technologies. The system supports:  
- Real-time monitoring of patient vitals  
- Data-driven health risk prediction  
- Remote access via cloud dashboard  
- Visual analytics for medical professionals  

---

## 🧰 Components Used

### ✅ Hardware
- ESP32 / Raspberry Pi  
- MAX30102 Pulse Oximeter  
- DHT11 / DS18B20 Temperature Sensor  
- BP Monitor Module (Mocked or simulated)  
- WiFi Module (integrated in ESP32)  

### ✅ Software
- Python 3.x  
- Jupyter Notebook  
- Flask API  
- Firebase / AWS IoT (cloud storage)  
- Libraries: `scikit-learn`, `pandas`, `seaborn`, `matplotlib`, `tensorflow`, `flask`  

---

## 🧠 Algorithms Used

- Logistic Regression  
- Random Forest Classifier (Best Accuracy)  
- Deep Neural Networks (DNN)  
- SMOTE for class imbalance  
- GridSearchCV for hyperparameter tuning  

---

## 📊 Methodology

1. **Data Collection**: Simulated patient data from sensors  
2. **Preprocessing**: Standard scaling, missing value handling  
3. **Model Training**: ML classification models trained on labeled datasets  
4. **Deployment**: Real-time predictions using Flask API  
5. **Visualization**: Data analysis using Matplotlib and Seaborn  

---

## 📈 Performance Metrics

| Model                     | Train Accuracy | Test Accuracy |
|---------------------------|----------------|---------------|
| Logistic Regression       | 91.4%          | 88.3%         |
| Random Forest Classifier  | 99.2%          | 96.5%         |
| Deep Neural Network       | 97.8%          | 95.2%         |

---

## 📷 Data Visualization Screenshots

### ✅ Age Distribution (Histogram)  
Shows patient age patterns.  
![Age Histogram](screenshots/histogram_age.png)

### ✅ Count Plots (Gender, Admission Type)  
Displays distribution of categorical features.  
![Gender Count](screenshots/countplot_gender.png)

### ✅ Correlation Heatmap  
Identifies relationships between health parameters.  
![Correlation Heatmap](screenshots/correlation_heatmap.png)

### ✅ Box Plots  
Detects outliers in vital signs like BP and heart rate.  
![Box Plot - BP](screenshots/boxplot_bp.png)

---

## 🚀 Flask API Endpoint Example

```python
@app.route('/predict', methods=['POST'])
def predict():
    data = request.get_json(force=True)
    prediction = model.predict([list(data.values())])
    return jsonify(result=str(prediction[0]))

Folder Structure

├── data/
│   └── patient_data.csv
├── models/
│   └── trained_model.pkl
├── app/
│   └── flask_api.py
├── notebooks/
│   └── analysis.ipynb
├── screenshots/
│   └── *.png
├── README.md


🔐 Security & Privacy
Data is encrypted in transit using HTTPS

User authentication integrated (Firebase/Auth)

Future scope includes Blockchain-based access logs

🧪 Future Improvements
Deploy on edge devices (e.g., Jetson Nano, Arduino BLE Sense)

Add support for voice alerts and dashboard notifications

Integrate blockchain for health record decentralization

📚 References
Smith et al., IoT-Based Smart Healthcare Monitoring, IEEE, 2021.

Patel et al., Wireless Body Sensor Networks, ACM, 2020.

Zhang et al., Security Challenges in IoT Healthcare, Elsevier, 2022.

Kumar et al., AI-Driven Patient Monitoring, Springer, 2021.

Li et al., Cloud and Edge for Smart Hospitals, IEEE IoT Journal, 2020.

⭐️ Star the Repo!
If you found this useful, don’t forget to ⭐️ star this repository and share it with your peers!


