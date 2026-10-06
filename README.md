## Project Overview

The goal of this project is to use **Linear Regression** to predict laptop prices based on:

- Brand
- Laptop Type
- Screen Size
- RAM
- Storage
- GPU Type

The project follows a simple ML workflow:

**Data Collection → Data Exploration → Preprocessing → Train/Test Split → Model Training → Evaluation → Prediction**

## Dataset

The project includes a small classroom-friendly dataset in:

`data/laptop_price_dataset.csv`

It contains 40 laptop records with prices in Indian Rupees.

## Machine Learning Algorithm

The project uses **Linear Regression**, a supervised learning algorithm used for regression problems.

Categorical features are converted using **One-Hot Encoding**, while numerical features are passed directly to the model. The preprocessing and model are kept together in a scikit-learn Pipeline so the same transformations are applied consistently during prediction.

## Project Structure

```text
Laptop-Price-Prediction/
│
├── data/
│   └── laptop_price_dataset.csv
│
├── notebooks/
│   └── Laptop_Price_Prediction.ipynb
│
├── models/
│   └── laptop_price_model.pkl
│
├── src/
│   ├── train_model.py
│   └── predict.py
│
├── requirements.txt
└── README.md
```

## Installation

Clone the repository and install the required packages:

```bash
pip install -r requirements.txt
```

## Run the Notebook

```bash
jupyter notebook
```

Open:

`notebooks/Laptop_Price_Prediction.ipynb`

## Train the Model

From the project root:

```bash
python src/train_model.py
```

The script prints the model's:

- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)
- R² Score

and saves the trained model to:

`models/laptop_price_model.pkl`

## Make a Prediction

Run:

```bash
python src/predict.py
```

Enter the laptop specifications when prompted. The program will return an estimated price in INR.

## Example

```text
Laptop Price Prediction
-----------------------
Brand (HP/Dell/Lenovo/ASUS/Acer/Apple/MSI): Lenovo
Type (Notebook/Ultrabook/Gaming): Gaming
Screen size in inches: 16
RAM in GB: 16
Storage in GB: 1024
GPU Type (Integrated/Dedicated): Dedicated

Estimated Laptop Price: ₹...
```

## Evaluation

The model is evaluated on data that was not used for training. MAE represents the average absolute prediction error, while R² indicates how much of the variation in the target is explained by the model.

## Future Improvements

- Use a larger real-world laptop dataset
- Add CPU and processor generation
- Add operating system
- Add laptop weight
- Add GPU model
- Compare Linear Regression with Random Forest Regression
- Build a simple web interface using Flask or Streamlit

## Technologies Used

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Jupyter Notebook

## Author

**Faraz Khan**

Academic Machine Learning Project
