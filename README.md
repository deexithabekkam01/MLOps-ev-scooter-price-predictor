EV Scooter Price Predictor 🛵
An end-to-end Machine Learning project designed to estimate the launch price of Electric Scooters based on technical specifications and brand positioning.

📋 Project Overview
1. Data Collection & Enhancement
Web Scraping: All raw data was scraped from Bikedekho, capturing various EV scooter models, prices, and technical specs.

Prompt Engineering: We used LLM-based prompt engineering to enhance the dataset, filling in missing details and structuring categorical information that was not easily available in raw form.

2. Exploratory Data Analysis (EDA) & Cleaning
Heatmap Analysis: We generated a correlation heatmap to identify which features actually influenced the price.

Feature Selection: Based on the EDA, we dropped "noisy" or redundant columns (e.g., url, variant, user_rating) that didn't provide predictive value.

Data Imputation: Handled missing values using median imputation to maintain a robust dataset of 364 entries.

3. Model Development & Optimization
We moved from basic testing to a highly tuned "honest" model:

Initial Evaluation: Tested 9 different models (Linear Regression, XGBoost, CatBoost, etc.).

Leakage Prevention: Identified and removed "leaky" features like price_per_km that were artificially inflating accuracy scores.

Hyperparameter Tuning: Performed a GridSearchCV on the Random Forest Regressor to find the optimal balance between depth and accuracy.

Final Performance: Achieved an R² score of 0.8748 and a Mean Absolute Error (MAE) of ₹10,433.

4. Web Deployment
Backend: Built a Flask application to serve the trained model.

Frontend: Created a clean, user-friendly interface for inputting scooter specs (Battery, Range, Speed, etc.).

Tunneling: Integrated ngrok to make the local development server accessible via a public URL for real-time testing.

5. Final Output:
<img width="1919" height="903" alt="image" src="https://github.com/user-attachments/assets/efc411d7-4fae-4682-9589-8833ae79d085" />


🛠️ Tech Stack
Python (Pandas, Numpy, Scikit-Learn)

Boosting Algorithms (XGBoost, CatBoost, LightGBM)

Web Framework (Flask)

Connectivity (Ngrok)
