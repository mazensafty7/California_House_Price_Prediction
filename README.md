# California House Price Prediction

The **California House Price Prediction** project focuses on estimating house prices in California using machine learning models. The models analyze various factors such as location, income, and property characteristics to predict house prices accurately.

![California House](https://github.com/user-attachments/assets/2ae1eb50-afc0-432e-b0ab-505c3aef5a67)

## Project Workflow

### 1. Data Exploration (EDA)
An in-depth exploration of the dataset was performed to understand the relationships between features like location, population, total rooms, and income levels, and how they influence house prices.

### 2. Data Cleaning and Preprocessing
Key steps in data cleaning and preprocessing:
- Handled missing values and outliers.
- Created new variables such as:
  - `bedrooms_ratio`: Ratio of bedrooms to total rooms.
  - `households_rooms`: Average number of rooms per household.
- Applied one-hot encoding to categorical variables like `OCEAN`.
- Used `MinMaxScaler` to normalize numerical features.

### 3. Data Analysis and Insights
Key insights from the data analysis:
- **Total Rooms and Population**: A positive correlation between areas with higher population density and total number of rooms.
- **House Age and Total Rooms**: Older houses tend to have fewer rooms.
- **Income and House Price**: Higher income areas generally correspond to higher house prices.
- **Proximity to Ocean**: Houses near the ocean tend to be more expensive, especially those within an hour’s proximity.
- **Geographic Insights**: Homes closer to the coast (higher longitude) tend to be more expensive than those further inland.

![California House Price Correlations](https://github.com/user-attachments/assets/828c79ab-608f-4602-a6cc-9b217008cce5)

**For more about correlations go to**: [California House Price Correlations](https://app.milanote.com/1SH6aN1JBYxAcm?p=ec7fAn22fDg)

### 4. Data Preparation for Modeling
- Addressed data skewness and missing values.
- Applied Min-Max scaling for numerical features.
- Split the data into training and testing sets for model evaluation.

### 5. Model Selection and Tuning

#### Decision Tree
The Decision Tree model was first used, optimized using GridSearch with cross-validation (`k=5`). The model produced the following results:
- **Training Score**: 0.8437
- **Test Score**: 0.7624
- **Best Parameters**: 
  - `max_depth`: 21
  - `min_samples_leaf`: 14
  - `min_samples_split`: 2

#### AdaBoost
Next, the AdaBoost model was tested, again using cross-validation (`k=5`), and achieved higher performance:
- **Training Score**: 0.8724
- **Test Score**: 0.8020
- **Best Parameters**:
  - `learning_rate`: 0.1
  - `n_estimators`: 35
  - `base_estimator`: `DecisionTreeRegressor(random_state=42)`
  - `base_estimator__max_depth`: 12
  - `base_estimator__min_samples_leaf`: 20
  - `base_estimator__min_samples_split`: 10

### 6. Final Model Selection
The **AdaBoost** model outperformed the Decision Tree model in terms of accuracy, making it the final selection for this project.

## Technologies Used
- **Data Analysis and Visualization**: Pandas, Numpy, Matplotlib, Seaborn
- **Data Preprocessing**: Handling missing data, Min-Max Scaler, One-hot Encoding
- **Machine Learning**: Decision Tree, AdaBoost
- **Model Evaluation**: Cross-validation, GridSearch, Model tuning , Learning Curves
