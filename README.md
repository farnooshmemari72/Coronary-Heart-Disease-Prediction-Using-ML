
# CHD Prediction Using Decision Support Systems

## Overview
This project was developed as part of a **Decision Support Systems** course to demonstrate the application of machine learning techniques for classification and decision-making. The focus was on predicting the likelihood of **Coronary Heart Disease (CHD)** using a dataset of health-related variables.

## Dataset
The dataset used for training and testing the model was sourced from **Mendeley Data**:  
[Dataset Link](https://data.mendeley.com/datasets/jc3rwftjnf/1)  
This dataset contains critical health indicators such as cholesterol levels, blood pressure, age, and other attributes relevant to predicting CHD outcomes.

## Project Steps
1. **Data Preparation and Cleaning**:
   - Loaded the dataset into a pandas DataFrame.
   - Inspected and preprocessed the data to handle any missing or inconsistent values.

2. **Fuzzyfication**:
   - Converted numerical features (e.g., cholesterol levels, blood pressure, age) into fuzzy membership values using fuzzy membership functions:
     - **Linear**: Ascending and descending functions.
     - **Triangular**: For features with a peak membership.
     - **Trapezoidal**: For features with a range of full membership.
   - This step enabled better handling of gradual transitions and uncertainty in the data.

3. **Feature Engineering**:
   - Generated fuzzy features such as:
     - Cholesterol: Low, Middle, High.
     - HDL, LDL, Blood Pressure (Systolic and Diastolic), and Age categories.
   - These features captured nuanced patterns in the data.

4. **Model Training**:
   - Split the dataset into training (70%) and testing (30%) subsets.
   - Trained a **Decision Tree Classifier** with hyperparameters optimized to prevent overfitting:
     - Maximum depth: 10.
     - Minimum samples to split: 20.
     - Minimum samples per leaf: 10.

5. **Model Evaluation**:
   - Evaluated the trained model using metrics like **accuracy**.
   - Computed and visualized the **confusion matrix** to assess performance across different classes.

6. **Decision Tree Visualization**:
   - Exported the trained decision tree as a graph using `export_graphviz` and visualized it for better interpretability.

## Results
- The decision tree model achieved a satisfactory level of accuracy in predicting CHD based on the given dataset.
- Visualization of the decision tree provided insights into the key features influencing the predictions.

## Conclusion
This project showcases the integration of fuzzy logic, machine learning, and data visualization to solve a real-world problem. The techniques used in this project demonstrate how Decision Support Systems can leverage data-driven insights to aid in critical health-related decision-making.

## Requirements
- Python 3.x
- Libraries: 
  - pandas
  - sklearn
  - pydotplus
  - matplotlib
  - seaborn
  - IPython
- Dataset: Download from [Mendeley Data](https://data.mendeley.com/datasets/jc3rwftjnf/1)

## How to Run
1. Clone this repository.
2. Install the required Python libraries.
3. Run the Jupyter Notebook file to reproduce the results.
4. Explore the decision tree visualization and confusion matrix outputs.

## License
This project is for educational purposes and is shared under the MIT License.

