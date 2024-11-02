# Fitness Dataset

This dataset contains fitness metrics and health information for individuals aged 20 to 64 years. It includes a variety of physical attributes, performance measures, and health metrics, which can be used for statistical analysis, machine learning modeling, and fitness classification tasks.

## Table of Contents

1. [Dataset Overview](#dataset-overview)
2. [Data Dictionary](#data-dictionary)
3. [Data Usage](#data-usage)
4. [Example Code](#example-code)

---

### Dataset Overview

- **Age Range:** 20 to 64 years
- **Purpose:** This dataset is ideal for exploring relationships between various physical metrics, assessing fitness levels, and developing predictive models for fitness classifications.
- **Potential Applications:** Statistical analysis, machine learning, health and fitness studies, and other research focusing on physical fitness and health.

---

### Data Dictionary

| Column Name                | Description                                                                                                    |
|----------------------------|----------------------------------------------------------------------------------------------------------------|
| **age**                    | Age of the individual (20-64 years).                                                                          |
| **gender**                 | Gender of the individual, represented by 'F' (Female) and 'M' (Male).                                         |
| **height_cm**              | Height in centimeters (to convert to feet, divide by 30.48).                                                  |
| **weight_kg**              | Weight in kilograms.                                                                                          |
| **body_fat_perc**          | Body fat percentage of the individual.                                                                        |
| **diastolic**              | Diastolic blood pressure (minimum), measured in mmHg.                                                         |
| **systolic**               | Systolic blood pressure (minimum), measured in mmHg.                                                          |
| **grip_force**             | Grip force, representing hand grip strength, measured in kilograms or newtons (units may vary).               |
| **sit_and_bend_forward_cm**| Distance reached while sitting and bending forward, measured in centimeters; often a measure of flexibility.  |
| **sit_ups_counts**         | Number of sit-ups performed by the individual, indicating abdominal strength or endurance.                    |
| **broad_jump_cm**          | Distance covered in a broad jump by the individual, measured in centimeters; assesses lower body power.       |
| **class**                  | Fitness classification of the individual, with possible categories 'A', 'B', 'C', and 'D'. 'A' denotes the best performance, and classes are stratified based on fitness levels. |

---

### Data Usage

This dataset can be used to:
- Calculate basic statistics, like mean, median, variance, and standard deviation for each numeric column.
- Compare fitness levels across different age groups, genders, or body types.
- Develop machine learning models for classification tasks, predicting an individual's fitness class based on other attributes.
- Analyze correlations between body fat percentage, blood pressure, and physical performance.

### Example Code

Here's an example of how to load and analyze this dataset using Python:

```python
import pandas as pd

# Load the dataset
df = pd.read_csv("fitness_data.csv")

# Display summary statistics
print(df.describe())

# Calculate correlations
correlations = df.corr()
print("Correlations:", correlations)

# Group by fitness class and calculate mean values
class_summary = df.groupby("class").mean()
print("Fitness Class Summary:", class_summary)
```