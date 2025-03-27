# Mushroom-Edibility-Classification
This project classifies mushrooms as edible or poisonous using their physical attributes. By analyzing a dataset with categorical features, the project employs data visualization and preprocessing techniques. A decision-tree classification model is used to distinguish between edible and poisonous mushrooms, providing an interpretable solution.

## Description
This project aims to classify mushrooms as edible or poisonous based on their physical attributes. Using the Mushroom Dataset from UCI's Machine Learning Repository, we build predictive models to assist foragers and researchers in identifying toxic mushrooms.

## Data Source
[Mushroom Dataset, UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Secondary+Mushroom+Dataset)

This dataset includes 61069 hypothetical mushrooms with caps based on 173 species (353 mushrooms per species italicized text). Each mushroom is identified as definitely edible, definitely poisonous, or of unknown edibility and not recommended (the latter class was combined with the poisonous class).

## Hypothesis
- Certain features like cap shape, gill color, and odor can help classify mushrooms as either edible or poisonous.
- The project aims to uncover patterns and relationships between mushroom attributes that are indicative of their toxicity, without using machine learning.

## Method and Procedure

1. **Data Collection and Preprocessing:**
   - **Technology Used:** `pandas`, `numpy`
   - **Description:** The dataset is loaded from the UCI Machine Learning Repository in CSV format using `pandas`. Missing values are handled, and categorical data (e.g., mushroom attributes like cap shape and gill color) are encoded into numerical representations using label encoding (`pandas`' `.factorize()` method) or one-hot encoding (`pandas`' `get_dummies()`).
   
   - **Steps:**
     - Download the dataset from the UCI Repository.
     - Load the data into a `pandas` DataFrame.
     - Clean the dataset by removing or filling missing values.
     - Encode categorical variables using appropriate encoding techniques.

2. **Data Exploration:**
   - **Technology Used:** `pandas`, `matplotlib`, `seaborn`
   - **Description:** After preprocessing, the dataset is explored to understand the distribution and relationships of various mushroom features (e.g., cap shape, spore print color, gill size). Basic statistical summaries and visualizations are created.
   
   - **Steps:**
     - Use `pandas` functions like `.describe()` and `.info()` to get a quick overview of the data.
     - Visualize the distribution of key features (e.g., cap shape, gill color, etc.) using `matplotlib` histograms and `seaborn` pair plots or violin plots.
     - Identify missing or skewed data and outliers using visual techniques.

3. **Data Analysis:**
   - **Technology Used:** `pandas`, `matplotlib`, `seaborn`
   - **Description:** Analyze the correlation between features and the target label (edible or poisonous). Use visual methods like correlation heatmaps and scatter plots to find any relationships.
   
   - **Steps:**
     - Compute the correlation matrix for numerical features using `pandas` `.corr()` and visualize it using a heatmap (`seaborn`'s `heatmap` function).
     - Investigate relationships between categorical variables and the target using `seaborn`'s `countplot` or `boxplot`.

4. **Data Visualization:**
   - **Technology Used:** `matplotlib`, `seaborn`
   - **Description:** Various plots and charts are created to visually understand the feature distribution and relationships. These visualizations help in identifying key attributes related to mushroom toxicity.
   
   - **Steps:**
     - Create bar plots, histograms, and box plots for features such as cap shape, spore print color, and gill color.
     - Generate pair plots or scatter plots to visualize relationships between different mushroom features.
     - Visualize target class distribution (edible vs poisonous) using pie charts or bar charts.

5. **Data Transformation:**
   - **Technology Used:** `pandas`, `sklearn.preprocessing`
   - **Description:** Transform categorical features into numerical values suitable for further analysis. One-hot encoding is used for nominal features (such as cap shape and gill color), while label encoding is applied to ordinal features.
   
   - **Steps:**
     - Apply `sklearn.preprocessing.LabelEncoder` for ordinal feature encoding.
     - Use `pandas.get_dummies()` for one-hot encoding of categorical features like cap shape or habitat type.
     - Normalize features if necessary using `sklearn.preprocessing.StandardScaler` or `MinMaxScaler`.

6. **Conclusion:**
   - **Technology Used:** `pandas`, `matplotlib`, `seaborn`
   - **Description:** Based on the visual analysis and correlation study, conclusions are drawn regarding which features are the most important in classifying mushrooms as edible or poisonous. Key features like odor, spore print color, and gill size are identified as significant.
   
   - **Steps:**
     - Summarize the findings based on feature importance from exploratory analysis.
     - Provide insights into how mushroom attributes can help in toxicity classification.

## Results
- Key features like spore print color, odor, and gill color have a strong correlation with mushroom toxicity.
- Visualization helped to identify how mushrooms with specific characteristics (e.g., odor) are more likely to be poisonous.
- While machine learning was not applied, this data analysis provided a solid understanding of which features matter most in classifying mushrooms.

## Breakdown of Technologies Used in Each Step:

- **Data Collection and Preprocessing:**
  - `pandas` is used to load and preprocess the dataset (handle missing values, encode categorical features).
  - `numpy` is used for numerical operations when handling data manipulation.

- **Data Exploration:**
  - `pandas` for descriptive statistics and inspecting the data.
  - `matplotlib` and `seaborn` are used for visualizations like histograms, bar plots, and pair plots.

- **Data Analysis:**
  - `pandas` is used to calculate correlations between features.
  - `seaborn` is used to visualize the correlation matrix and relationships between features and target labels.

- **Data Visualization:**
  - `matplotlib` and `seaborn` are heavily used for generating plots (histograms, box plots, scatter plots) to understand the feature distributions and relationships.

- **Data Transformation:**
  - `sklearn.preprocessing` provides tools like `LabelEncoder` for ordinal encoding and `get_dummies()` for one-hot encoding.
  - Scaling features is done using `MinMaxScaler` or `StandardScaler` from `sklearn`.

This README is now more detailed and includes the specific technologies used for each step in the project. Let me know if you need further modifications!

## Pre-Requisites and System Requirements

- **Programming Language:** Python 3.x
- **Libraries:**
  - `pandas` for data manipulation and analysis
  - `numpy` for numerical operations
  - `matplotlib` for basic data visualization
  - `seaborn` for advanced visualizations
  - `sklearn.preprocessing` for encoding categorical data and normalizing features
- **System Requirements:** 
  - Minimum 4 GB RAM
  - Jupyter Notebook or Google Colab for executing the code
  - Internet connection to download the dataset from UCI's Machine Learning Repository

## How to Run
1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/mushroom-classification.git
   ```

2. Install the required libraries:
   ```
   pip install -r requirements.txt
   ```
3. Open the project in Jupyter Notebook or Google Colab.
4. Run the notebook file `(mushroom_classification_analysis.ipynb)` to start analyzing the dataset.

## Future Studies
1. Explore more advanced data transformation techniques such as feature engineering or feature selection methods.

2. Investigate using machine learning models like Decision Trees or Random Forests for automated classification of mushrooms based on their attributes.

3. Extend the project to include other datasets related to plant or food classification to identify patterns across different species.
   
