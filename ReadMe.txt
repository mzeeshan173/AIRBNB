
# Classifying Airbnb Listings into Price Bands

This project aims to classify Airbnb listings into three price bands (Low, Mid, High) based on features such as location, room type, and availability. It uses various machine learning models, including **Random Forest**, **Support Vector Machines (SVM)**, and **K-Nearest Neighbors (KNN)**, to classify listings. The notebook also utilizes **Explainable AI** methods like **Gini Importance** for feature interpretation and model transparency.

## **Research Questions**
1. How accurately can machine learning models classify Airbnb listings into price bands based on the features provided?
2. Which features are the most influential in determining the price band, and how can we interpret the model’s decisions?
3. How does the model performance compare across different algorithms, and how can we address model fairness and performance balance?

## **Dataset Details**
- **Name:** Airbnb Listings Dataset
- **Source:** The dataset contains information on Airbnb listings, including pricing, room types, geographic location, and host details.
- **Contributors:** Data was collected from publicly available Airbnb listings, showcasing a wide range of attributes like room types, neighborhood groups, availability, and number of reviews.

## **Libraries Used**
- **pandas** for data manipulation and preprocessing.
- **matplotlib** and **seaborn** for data visualization.
- **scikit-learn** for machine learning models and evaluation metrics.
- **SHAP** for model interpretability and feature importance analysis.

## **Steps Performed in the Notebook**
1. **Import Libraries:** All necessary libraries are imported for data manipulation, model building, and evaluation.
2. **Load Dataset:** The Airbnb listings dataset is loaded and previewed to inspect its structure and content.
3. **Data Preprocessing:**
   - Removed irrelevant columns such as `id`, `name`, and `license`.
   - Cleaned and converted the `price` column by removing special characters and converting values to numeric types.
   - Handled missing values by filling numerical columns (like `price`) with the median and textual columns (e.g., `last_review`) with `"No Review"`.
   - Dropped rows with missing values in essential columns like `room_type` and `neighbourhood`.
   - Removed outliers by excluding listings with prices above the **95th percentile**.
   - Created a new target variable `price_band` by dividing prices into three bands — **Low**, **Mid**, and **High**.
4. **Model Training:**
   - Trained **Random Forest**, **Support Vector Machines (SVM)**, and **K-Nearest Neighbors (KNN)** models to classify listings into price bands.
5. **Hyperparameter Tuning:** Tuned hyperparameters using **GridSearchCV** to optimize model performance.
6. **Model Evaluation:** Evaluated model performance using metrics like accuracy, precision, recall, and F1-score.
7. **Explainable AI (Gini Importance):** Used Gini importance from the Random Forest model to interpret the most influential features affecting the price band classification.
8. **Final Visualization:** Plotted the Gini importance and performance metrics to visualize the impact of various features on the model’s predictions.

## **How to Run the Notebook**
1. Clone the repository to your local machine.
2. Install the required libraries:
   ```bash
   pip install pandas matplotlib seaborn scikit-learn shap
   ```
3. Download the **Airbnb Listings Dataset** or use your own dataset structured similarly.
4. Open the notebook in **Jupyter Notebook** or **Google Colab**.
5. Execute all the cells to perform data preprocessing, model training, and performance evaluation.

## **Results**
The project compares multiple machine learning models for classifying Airbnb listings into price bands. The models' performances are evaluated, and SHAP and Gini importance provide insights into the most influential features. The Random Forest model performs particularly well due to its handling of feature interactions and nonlinearities.

## **Contributions**
Feel free to contribute by:
- Adding more machine learning algorithms for price band classification.
- Enhancing data preprocessing and feature engineering techniques.
- Improving model interpretability and fairness.


