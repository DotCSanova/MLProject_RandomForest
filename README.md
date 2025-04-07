# 🧠 Automatic Indoor Occupancy Detection using Machine Learning

This project focuses on the automatic detection of indoor space occupancy using environmental sensor data. By leveraging a **Random Forest** classifier and optimization techniques like **Grid Search** and **Cross-Validation**, the goal is to accurately classify whether a given space is occupied or not, based on sensor inputs such as temperature, humidity, light, and CO₂ levels.

---

## 🔍 Problem Statement

Efficient space management and energy optimization require reliable detection of room occupancy. Instead of relying on cameras or manual checks, this project utilizes sensor data to infer occupancy status in a non-intrusive and scalable way.

---

## 🛠️ Approach

- **Model**: `RandomForestClassifier` from scikit-learn  
- **Data Inputs**: Temperature, Humidity, Light, CO₂  
- **Target**: Binary classification of room occupancy (Occupied / Not Occupied)

### Workflow

1. **Data Cleaning**:
   - Imported raw data from `datasetEn.csv`
   - Removed `NaN` values to ensure model stability and performance

2. **Feature Engineering**:
   - Features (`X`) include all sensor readings
   - Target (`y`) is occupancy status

3. **Model Training**:
   - Data split into 80% training and 20% testing sets
   - Initial model trained using default `RandomForestClassifier`

4. **Evaluation**:
   - Achieved ~94% accuracy on test data

5. **Model Optimization**:
   - Applied **GridSearchCV** with 5-fold cross-validation
   - Tuned `n_estimators` and `max_depth` parameters
   - Best parameters found: `n_estimators=140`, `max_depth=None`

6. **Prediction**:
   - Used the optimized model to classify a new, unlabelled dataset (`dataset_unclassified.csv`)
   - Results exported to `classification_estimated.csv`

---

## 📁 Files

- `datasetEn.csv` – Original labeled dataset used for training  
- `dataset_unclassified.csv` – New observations to classify  
- `classification_estimated.csv` – Output file containing model predictions  
- `RF_ocupation_detection.ipynb` – Full code with training, optimization, and prediction pipeline  

---

## 📈 Results

- Final model accuracy: **~94%**
- Successfully classified unseen data using the optimized model

---

## 🧰 Technologies Used

- uv
- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Jupyter Notebook  

---

## 🚀 Future Improvements

- Test other models (e.g., Gradient Boosting, XGBoost)
- Add time-based features or sensor fusion techniques
- Deploy as an API or integrate with smart building systems

---

## 👤 Author

**Alberto López Casanova**  
[LinkedIn](https://www.linkedin.com/in/alcasanova99/) • [GitHub](https://github.com/DotCSanova) • [Email](mailto:albertolopezcasanova@icloud.com)