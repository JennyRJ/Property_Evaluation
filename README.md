# Getting Started with a ML Property Evaluation Model in Python

---

## 1. Title & Objective

### Title

Building a Property Evaluation Web App using Python and ML

### Objective

This project aims to build a machine learning-based web application that predicts property prices using user inputs like location, size, and number of rooms.

### Technology Chosen

* Python
* Flask
* Scikit-learn
* Pandas
* NumPy

### Why this tech stack?

* Python is widely used in AI/ML
* Scikit-learn provides ready-made ML models
* Flask allows quick web app development

### End Goal

A working web app that takes property details and returns a predicted price.

---

## 2. Quick Summary of the Technology

### What is Scikit-learn?

Scikit-learn is a Python library used for building machine learning models such as regression, classification, and clustering.

### Where is it used?

* Predicting house prices
* Fraud detection
* Customer segmentation

### Real-world example

Real estate platforms use ML models to estimate property prices automatically.

---

## 3. System Requirements

* OS: Windows / Linux / Mac
* Editor: VS Code / PyCharm
* Python Version: 3.8+
* Required tools:

  * pip
  * virtual environment (venv)

### Required packages

```bash
pip install flask pandas numpy scikit-learn xgboost
```

---

## 4. Installation & Setup Instructions

### Step 1: Create project folder

```bash
mkdir property-evaluation-model
cd property-evaluation-model
```

### Step 2: Create virtual environment

```bash
python -m venv venv
venv\Scripts\activate
```

### Step 3: Install dependencies

```bash
pip install flask pandas numpy scikit-learn xgboost
```

### Step 4: Run the Flask app

```bash
python app.py
```

---

## 5.  Minimal Working Example

### What this does

This example shows how to train a model used to predict property prices using the saved pipeline.

```python
import pickle
import pandas as pd

# Load trained model
model = pickle.load(open('RegressorModel.pkl', 'rb'))

# Example input (must match training columns)
input_data = pd.DataFrame([[
    "Parklands, Westlands",
    3000,
    3,
    3
]], columns=['location','total_sqft','Bedrooms','Bathrooms'])

# Make prediction
prediction = model.predict(input_data)

print("Predicted Price:", prediction[0])
```

### Expected Output

```
Predicted Price: <some value based on model>
```

---

## 6. AI Prompt Journal

### Prompt used

“Give me a step-by-step guide to build a property price prediction model using Python and scikit-learn”

### AI response summary

The AI provided steps for dataset loading, model training, preprocessing, and deployment structure.

### Useful insight

The AI helped structure the ML pipeline and explained how preprocessing connects to prediction.

### Evaluation

Very helpful for understanding the full workflow from data → model → deployment.

---

## 7. Common Issues & Fixes

### Issue 1: 'str' object has no attribute 'transform'

Fix: Ensure pipeline uses real transformers, not strings.

### Issue 2: Module not found

Fix:

```bash
pip install scikit-learn pandas numpy
```

### Issue 3: Flask app not running

Fix:

* Ensure app.py is in correct directory
* Activate virtual environment before running

---

## 8. References

* Scikit-learn documentation
* Flask documentation
* NumPy documentation
* Kaggle datasets
* StackOverflow

---

## Final Note

This project demonstrates a full machine learning pipeline from data preprocessing to deployment using Flask.
