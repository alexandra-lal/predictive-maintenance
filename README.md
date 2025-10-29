# Predictive Maintenance Model
This project demonstrates a Predictive Maintenance machine learning model that identifies whether a machine is likely to fail based on real sensor data.

The model uses a Random Forest Classifier trained on industrial IoT sensor readings such as air temperature, process temperature, rotational speed, torque, and tool wear.

---

# Project Structure
- <b>notebook.ipynb</b> - Jupyter notebook containing data analysis, training, and evaluation<br>
- <b>requirements.txt</b> - Dependencies used<br>
- <b>ai4i2020.csv</b> - Dataset (or sample of it)<br>
- <b>.gitignore</b> - Ignored environment and cache files

---

# Workflow

1. **Data Preprocessing**  
   - Encoded categorical features (machine type)  
   - Split dataset into training and test sets (80/20)  

2. **Model Training**  
   - Algorithm: `RandomForestClassifier`  
   - Trained using 8000 records  
   - Evaluated on 2000 test samples  

3. **Performance**  
   | Metric | Score |
   |:-------|:------|
   | Accuracy | **98.4%** |
   | Precision | 0.99 (class 0), 0.84 (class 1) |
   | Recall | 1.00 (class 0), 0.59 (class 1) |

4. **Feature Importance**  
   - The most influential features:  
     - **Torque (Nm)**  
     - **Rotational Speed (rpm)**  
     - **Tool Wear (min)**

---

# Results

| Feature | Importance |
|:--------|:------------|
| Torque (Nm) | 0.30 |
| Rotational Speed (rpm) | 0.23 |
| Tool Wear (min) | 0.17 |
| Air Temperature (K) | 0.14 |
| Process Temperature (K) | 0.13 |
| Machine Type | 0.03 |

[Feature Importance Plot](images/feature_importance.png)

---

# Tools & Libraries

- Python 3.x  
- Pandas  
- Scikit-learn  
- Matplotlib  
- NumPy

---

# How to Run

1. **Clone this repository**  
   ```bash
   git clone https://github.com/alexandra-lal/predictive-maintenance.git
   cd predictive-maintenance

2. **Install dependencies**  
   ```bash
   pip install -r requirements.txt

3. Open the Jupyter Notebook
   ```bash
   jupyter notebook notebook.ipynb

---

# Insights

Through this project, I explored how machine learning can anticipate equipment failures before they happen — reducing downtime and optimizing maintenance schedules.  

- The **Random Forest** model delivered strong accuracy (98.4%) and excellent precision, showing it can reliably distinguish between normal and at-risk machine states.  
- **Torque**, **rotational speed**, and **tool wear** emerged as the most significant indicators of potential failure.  
- The model slightly underperformed on minority (failure) cases, suggesting future improvements with resampling or cost-sensitive learning techniques.  
- The analysis demonstrates how predictive maintenance can directly translate to operational efficiency and cost savings in industrial environments.  

---

# Author

- [GitHub](https://github.com/alexandra-lal)  

---

# Future Enhancements

- TBD


