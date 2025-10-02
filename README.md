# Iris Flower Type Prediction

This project is a web application built with Streamlit that predicts the type of iris flower based on user inputs of flower features: Sepal Length, Sepal Width, Petal Length, and Petal Width. The model is trained using the popular Iris dataset with a Linear Regression model, and target classes are encoded using `LabelEncoder`.

---

## Features

- Interactive UI for entering iris flower measurements.
- Real-time prediction of iris species using a trained machine learning model.
- Uses a pre-trained Linear Regression model and LabelEncoder saved as `.pkl` files.
  
---

## Getting Started

### Prerequisites

- Python 3.7 or above
- Install required packages from `requirements.txt`

### Installation

1. Clone this repository:
`git clone <repository-url>`

`cd <repository-folder>`


2. Place the following pickle files inside the root project folder (same location as `app.py`):
- `model.pkl` (the trained Linear Regression model)
- `label.pkl` (the fitted LabelEncoder for class labels)

3. Install dependencies:
`pip install -r requirements.txt`

### Running the App

Run the Streamlit app using:
`streamlit run app.py`

Open the displayed URL (usually `http://localhost:8501`) in your browser to interact with the app.

---

## Project Structure


├── `app.py # Streamlit frontend and prediction logic`

├── `model.pkl # Serialized trained model file (pickle)`

├── `label.pkl # Serialized fitted LabelEncoder (pickle)`

├── `Iris.ipynb # Jupyter notebook for training and experimentation`

├── `requirements.txt # Python dependencies`

└── `README.md # Project readme file`

---

## Key Points and Notes

- The model must be trained and saved before running Streamlit. Training happens in `Iris.ipynb`.
- `model.pkl` and `label.pkl` must be present in the same directory as `app.py` for the app to load and use.
- The LabelEncoder is fit on the training labels to convert numeric predictions back to original species names.
- If training a new model, ensure you save both the trained model and the LabelEncoder.
- Predictions are converted from numeric output to categorical species using `le.inverse_transform` properly.
- This project uses Linear Regression, generally suitable for continuous targets, but here it models classification by encoding species as numeric.

---

## Dependencies

Refer to `requirements.txt` for all Python libraries needed to run the app.
