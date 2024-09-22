# Side Effect Analysis Project

**Gamze Genç**
**Email:gamzegen99@gmail.com**

## 1. Introduction

### Project Overview
This project aims to analyze the relationships between drug usage, patient characteristics, and side effects using the "`side_effect_data.xlsx`" dataset. 
The dataset contains 2,357 rows and 19 columns, which provide information on various patient demographics and their experiences with medications.

The main tasks include:
- Exploratory Data Analysis (EDA)
- Data Pre-Processing for future predictive modelling

### Instructions to Run the Code
- Ensure you have Python and the necessary libraries installed (Pandas, Seaborn, Matplotlib, Scikit-learn).
- Open the Jupyter Notebook `eda_and_preprocessing.ipynb` and run the cells sequentially.

### Required Libraries
- Pandas
- Seaborn
- Numpy
- Matplotlib
- Scikit-learn
- 
### Problem Definition
Medication side effects are a significant concern for patient health and safety. This project analyzes the dataset to identify factors that may influence medication side effects and to develop a machine learning model that can potentially be used to predict the risk of side effects.
### Questions
- Which medications cause which side effects more frequently?
- How do patient demographics (gender, age, etc.) and health history (allergies, chronic diseases, etc.) affect the risk of side effects?
- Is there a relationship between body mass index (BMI) and side effects?
- Does the duration of medication use increase the likelihood of side effects?
- 
## 2. Introduction of Dataset
The dataset used in this project consists of an Excel file (side_effect_data.xlsx) containing information about patients' medication use, personal information, and side effects they experience.

### Dataset Size
The dataset contains a total of 2357 rows and 19 columns.

### Variables
- **Demographic Information:** Gender, Age, Height, Weight, Province, Nationality(Cinsiyet, Yaş, Boy, Kilo, İl, Uyruk)
- **Health History:** Allergies, Chronic Diseases, Chronic Diseases in the Family (Mother, Father, Siblings) -(Alerjiler, Kronik Hastalıklar, Ailede Kronik Hastalıklar (Anne, Baba, Kardeşler))
- **Drug Information:** (İlaç Adı, İlaç Başlangıç Tarihi, İlaç Bitiş Tarihi)Drug Name, Drug Start Date, Drug End Date
- **Side Effect Information:** Side Effect, Side Effect Report Date (Yan Etki, Yan Etki Bildirim Tarihi) 
- **Other:** Blood Group, User ID (Kan Grubu, Kullanıcı ID)
- 
## 3. Exploratory Data Analysis (EDA)

### Data Structure
The dataset contains a mixture of numerical and categorical variables.
- **Numeric Variables:** Height, Weight, Age
- **Categorical Variables:** Gender, Province, Name of Medication, Side Effect, My Allergies, My Chronic Diseases, Family Chronic Diseases

### Visualizations
- **Histograms:** To understand the distribution of numerical variables.
- **Box Plots:** To visualize outliers.
- **Scatter Plots:** To examine the relationship between Height and Weight.
- **Count Plots:** To visualize the frequencies of categorical variables and the relationships between some variables.

### Key Findings
- The most common side effects were identified. (A Different Taste in the Mouth, Increased Blood Pressure, etc.)
- Lurasidone is the drug with the most side effects.
- Differences were observed between gender and side effects.

## 4. Data Preprocessing

### Deriving New Variables
- **Duration of Drug Use:** Calculated using drug start and end dates.
- **Duration of Side Effect Emergence:** Calculated using side effect notification date and drug start date.
- **BMI:** Calculated using Weight and Height variables and categorized.

### Missing Data Management
- **Numerical Variables:** Filled with Mean.
- **Categorical Variables:** Filled with "Unknown" value.

### Coding of Categorical Variables
- **Label Encoding:** Gender and Blood Group variables.
- **One-Hot Encoding:** City, Drug Name, Side Effect and Allergies variables.
- **Ordinal Encoding:** BMI_category variable.

### Normalization/Standardization
Numeric variables are standardized.

### Dimensionality Reduction Techniques: PCA Analysis
- The dimensionality of the dataset was reduced by applying PCA. The original dataset was reduced from (2357, 281) to (2357, 47).

## 5. Analysis Results

### Side Effect Distribution According to BMI Categories
- More number and variety of side effects were observed in obese individuals.

## Conclusion
Data preprocessing stage increased the quality of the data and will help the model produce more accurate and reliable results.


## Additional Information
- The dataset is located in the `side_effect_data.xlsx` file.
- All findings and steps taken during data processing are documented in the notebook.

