# Enhancing Sniffing Detection in IoT Home Wi-Fi Networks using Ensemble Learning

This project detects passive sniffing attacks in IoT home Wi-Fi environments using ensemble machine learning models supported by real-time system monitoring via Network Monitoring System (NMS).

---

## 🔍 Overview
Sniffing attacks are difficult to detect in wireless IoT setups because they operate passively with minimal network footprints.  
This work introduces a machine learning approach trained on performance metrics collected from a monitored IoT device to classify whether sniffing activity is present.

---

## 🧠 Machine Learning Models Used
| Model | Type | Purpose |
|-------|------|---------|
| Decision Tree | Baseline | Model interpretability & feature behaviour analysis |
| Random Forest | Bagging | Robust multi-tree classification |
| XGBoost | Boosting | Fast, accurate gradient-based boosting |
| LightGBM | Boosting | Lightweight, parallel boosting with high performance |

All models underwent:
- Data preprocessing
- Outlier removal (Local Outlier Factor)
- Correlation-based feature reduction
- 10-fold Cross-Validation
- Train/Test evaluation (80:20)

---

## 🧪 Dataset Details
- **Total Samples:** 12,000  
- **Features:** 31 system & network metrics  
- **Monitored Parameters:**
  - CPU utilization
  - Memory usage
  - Disk writes
  - Network traffic
  - Ping response
  - System load  
- **Class Labels:** 10 sniffing scenarios (program type + load condition)

Dataset generated from real experimental Wi-Fi lab setup.

---

## 📊 Results
- ML models achieved **>99% accuracy**
- 7 key features strongly impact detection performance:
  - Memory usage
  - CPU load
  - Disk write volume
  - Network traffic patterns

LightGBM trained fastest while maintaining high precision.

---

## 📌 Conclusion
Using ensemble machine learning along with NMS monitoring significantly improves the ability to detect passive sniffing behaviour in IoT home Wi-Fi setups.  
This approach outperforms traditional RT-time or challenge-based methods and supports scalable security in smart networks.

