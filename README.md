# Heart Disease Classification Model

This repository contains a deep learning model implemented with TensorFlow to classify whether a patient has heart disease based on several health metrics. The model has been trained using real-world patient data and achieves high performance in terms of precision, recall, and F1 score.

## Model Overview

This project uses a neural network-based classification model to predict the presence of heart disease based on 11 input features. The features are normalized using the mean and scale values derived from the training data.

### Input Features:
1. **Age**: Patient's age (in years).
2. **Sex**: Gender of the patient (0 = female, 1 = male).
3. **Chest Pain Type**: 
   - 0: Typical Angina
   - 1: Atypical Angina
   - 2: Non-anginal Pain
   - 3: Asymptomatic
4. **Resting Blood Pressure**: Resting blood pressure (in mm Hg).
5. **Cholesterol**: Serum cholesterol (in mg/dl).
6. **Fasting Blood Sugar**: (1 = fasting blood sugar > 120 mg/dl, 0 = otherwise).
7. **Resting ECG**: Resting electrocardiographic results (0-2).
8. **Max Heart Rate**: Maximum heart rate achieved during exercise.
9. **Exercise Induced Angina**: (1 = Yes, 0 = No).
10. **Oldpeak**: ST depression induced by exercise relative to rest.
11. **ST Slope**: 
   - 0: Upsloping
   - 1: Flat
   - 2: Downsloping

### Output (Target):
- **Target**: Binary classification:
  - 0: No heart disease
  - 1: Heart disease

## Model Performance

The model was trained over 38 epochs with a batch size of 32, achieving the following performance metrics on the test set:

- **Precision**: 0.9984
- **Recall**: 0.9873
- **F1 Score**: 0.9928

### Confusion Matrix:
```
[[560   1]
 [  8 621]]
```

## Model Inference

You can interact with the model using a web interface implemented in TensorFlow.js. The model predicts whether a patient has heart disease based on input features.

### Inference Example:

```html
<form>
  <!-- Form to collect age, sex, and other health metrics -->
</form>

<script>
  // TensorFlow.js model inference script
  const input = [age, sex, chest_pain_type, resting_bp_s, cholesterol, fasting_blood_sugar, resting_ecg, max_heart_rate, exercise_angina, oldpeak, st_slope];
  // Normalize and predict using the model
</script>
```

## Installation

1. **Clone the repository**:
   ```bash
   git clone https://github.com/sebukpor/heart-disease-prediction.git
   cd heart-disease-prediction
   ```

2. **Install the required dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

3. **Run the model**:
   - You can use the provided Jupyter notebook to train and evaluate the model.
   - Alternatively, you can convert the model to TensorFlow.js for web-based inference.

## Usage

1. **Training**:
   - Use the provided script or Jupyter notebook to train the model on your data.
   - Ensure that you have the correct input features in the specified format.

2. **Inference**:
   - You can use the TensorFlow.js model for browser-based inference, allowing patients or healthcare professionals to input data and receive predictions.


## Credits

- [Divine Sebukpor](https://github.com/sebukpor) - Model development and deployment.

## License

This project is licensed under the MIT License.
