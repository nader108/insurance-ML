# Insurance Charges Prediction Model

This project focuses on predicting medical insurance charges based on various features like age, BMI, smoking habits, and region using a machine learning model. The model utilizes the Mean Squared Error (MSE) and R-squared (R²) to evaluate its performance.

Key Steps and Insights:
Data Preprocessing:

The dataset has been cleaned by removing duplicates and handling missing values, ensuring that the data used for training is consistent.
Outliers were detected and removed in the bmi and charges columns.
Model Performance:

Mean Squared Error (MSE): The MSE value is calculated as follows:
𝑀
𝑆
𝐸
=
1
𝑛
∑
𝑖
=
1
𝑛
(
𝑦
𝑖
−
𝑦
^
𝑖
)
2
MSE= 
n
1
​
  
i=1
∑
n
​
 (y 
i
​
 − 
y
^
​
  
i
​
 ) 
2
 
After calculating, we take the square root of the MSE to get the RMSE value of 1417.81.
R-Squared (R²): This value is used to measure the model's accuracy, which is 0.92, indicating that the model can explain about 92% of the variance in the insurance charges data.
Visualization:

Actual vs. Predicted: A scatter plot shows how the actual values compare to the predicted values.
Charges Comparison: A line plot compares the original charges (y_test) and the predicted charges (y_pred) after multiplying by 3.
Model Evaluation:

The model's prediction accuracy is verified by comparing the actual charges to the predicted charges.
MSE and R²: MSE is calculated, and the R² value indicates a good fit of the model to the data.
Visualizations 📊:
1. Actual vs Predicted Values
A scatter plot to compare the actual and predicted values for insurance charges:

python
Copy code
plt.scatter(y_test, y_pred, color='blue')
plt.title('Actual vs. Predicted Values')
plt.xlabel('Actual Values')
plt.ylabel('Predicted Values')
2. Charges vs. Predicted Charges
A line plot showing how the actual charges (scaled by a factor of 3) compare with the predicted charges (also scaled by 3):

python
Copy code
plt.plot(y_test*3, y_test, label='Original')
plt.plot(y_pred*3, y_pred, label='Predicted')
plt.legend()
3. Mean Squared Error and R-Squared
RMSE: After calculating MSE, we take the square root to get the final Root Mean Squared Error (RMSE).

python
Copy code
np.sqrt(mean_squared_error(y_test, y_pred))
The RMSE value is 1417.81.

R-Squared (R²): The model’s R² value of 0.92 indicates the goodness of fit.

python
Copy code
r_squared = r2_score(y_test, y_pred)
How to Use:
Clone this repository:
bash
Copy code
git clone https://github.com/your_username/Insurance-Charges-Prediction.git
Install the required libraries:
bash
Copy code
pip install -r requirements.txt
Open the Jupyter notebook or Python script to run the model and visualizations.
Contributions:
Feel free to contribute by submitting issues or pull requests!

