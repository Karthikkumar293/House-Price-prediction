# House-Price-prediction
🏡 California Housing Price Prediction
This project aims to predict California housing prices using various regression techniques, including Linear Regression, Ridge, Lasso, Decision Tree, and Random Forest. It uses the built-in California Housing dataset from Scikit-learn.

# 📁 Dataset
The dataset is fetched using:

python
Copy
Edit
from sklearn.datasets import fetch_california_housing
It includes 20,640 entries with the following features:

MedInc: Median income in block group

HouseAge: Median house age in block group

AveRooms: Average number of rooms per household

AveBedrms: Average number of bedrooms per household

Population: Block group population

AveOccup: Average house occupancy

Latitude: Block group latitude

Longitude: Block group longitude

Target: Median house value (in $100,000s)

# 🔧 Model Training
1. Linear Regression
Training Score: ~0.607

2. Ridge Regression (α=10)
Training Score: ~0.607

3. Lasso Regression
Training Score: Slightly lower than Ridge/Linear

4. Decision Tree Regressor
Training Score: 1.0 (Overfitting)

Test Score: ~0.582

5. Random Forest Regressor
Training Score: ~0.97

Cross-validation Score: ~0.65 (5-fold CV)

# 📈 Model Used for Final Prediction
The final model used is RandomForestRegressor with n_estimators=200 due to its superior performance and generalization (based on cross-validation).

# 🧪 Example Input Format
User is prompted to enter values in comma-separated format for the following 8 features:

mathematica
Copy
Edit
MedInc, HouseAge, AveRooms, AveBedrms, Population, AveOccup, Latitude, Longitude
Example Input:
Copy
Edit
8.3252, 41.0, 6.9841, 1.0238, 322.0, 2.5556, 37.88, -122.23
Example Output:
makefile
Copy
Edit
Prediction: [4.4112404]
# ⚠️ Warnings
You may encounter this warning:

r
Copy
Edit
UserWarning: X does not have valid feature names, but RandomForestRegressor was fitted with feature names
This is safe to ignore for small manual predictions. For production use, ensure the input is passed as a DataFrame with proper feature names.

# 🚀 How to Run
bash
Copy
Edit
python california_housing.py
Or in a Jupyter Notebook, run all cells from top to bottom. Make sure to enter the input when prompted.

# 📚 Requirements
Python 3.x

pandas

numpy

scikit-learn

seaborn

matplotlib

# Install dependencies using:

bash
Copy
Edit
pip install -r requirements.txt
# 📌 Notes
Consider hyperparameter tuning for further improving model accuracy.

You may use StandardScaler for scaling features or PCA for dimensionality reduction if needed.

Avoid using a single decision tree model due to overfitting.


