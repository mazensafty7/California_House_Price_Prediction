# California House Price Prediction - Decision Tree Model

![California House](https://github.com/user-attachments/assets/2ae1eb50-afc0-432e-b0ab-505c3aef5a67)

## Project Overview
This project involves predicting house prices in California using a Decision Tree model. The dataset contains various features like location, population, total rooms, and income levels, which are used to build a model that estimates property prices. The analysis dives deep into relationships between features to provide insights into factors influencing house prices in the region.

## Dataset
The dataset consists of features such as:
- **Longitude & Latitude**: Geographic coordinates.
- **Housing Median Age**: Age of the houses.
- **Total Rooms, Bedrooms, Population**: Key indicators of housing density.
- **Median Income**: Average income of the households.
- **Ocean Proximity**: The proximity of houses to the coast.

## Data Preprocessing
The data preprocessing steps included:
1. Handling missing values and outliers.
2. Feature engineering to create useful variables like `bedrooms_ratio` and `households_rooms` and `one hot encoding in OCEAN`.
3. Scaling numerical features using `MinMaxScaler`.

## Model Training
The data was split into training and test sets, and a Decision Tree model was trained using GridSearch with 5-fold cross-validation to optimize hyperparameters:
- **Optimal Parameters**:
  - `max_depth`: 21
  - `min_samples_leaf`: 13
  - `min_samples_split`: 2

- **Training Score**: *0.8489*
- **Testing Score**: *0.7632*

## Insights and Relationships

### Key Insights:
1. **Population and Total Rooms**: Higher population areas tend to have more total rooms, leading to a positive correlation.
2. **House Age vs. Total Rooms**: Older houses generally have fewer rooms, showing a negative correlation.
3. **Income and House Price**: Areas with higher median income have higher house prices, reflecting a strong positive correlation.
4. **Proximity to Ocean**: Houses closer to the ocean tend to be more expensive, with a high median income rate, especially near ocean less than 1 hour.
5. **Longitude and Latitude**: Homes closer to the west (higher longitude) and nearer to the ocean have higher prices, while those further inland (lower longitude) are less expensive.
   **For more about correlations go to**: [California House Price Correlations](https://app.milanote.com/1SH6aN1JBYxAcm?p=ec7fAn22fDg)

![California House Price Prediction](https://github.com/user-attachments/assets/828c79ab-608f-4602-a6cc-9b217008cce5)

### Storytelling:
- Houses near the Ocean Area tend to have higher prices due to their prime location. These homes often belong to wealthier individuals, reflected in the higher median income. Additionally, houses with more rooms often accommodate larger populations, driving up demand and prices. On the other hand, inland areas have lower prices, partially because they are farther from the ocean and less attractive to high-income buyers.

## Conclusion
This project demonstrates the effectiveness of using a Decision Tree model in predicting house prices while highlighting key factors driving property values in California.

## Additional Techniques Used:
- Learning curves and model complexity were utilized to handle overfitting and underfitting.
- Dealing with large datasets and cleaning them, including handling outliers and missing values.
- Feature engineering was employed to create new variables highly correlated with the target.
- MinMaxScaler was used to scale the data, and log transformation was avoided.
