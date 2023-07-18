<h1> Project Summary </h1>

Currently, we have a dataset from an ongoing cardiovascular study in residents of the town of Farmingham, Masschusets. The dataset contains the various information regarding the patients' health conditions and personal traits. It includes nearly 3000 records and 17 attributes. Each attribute is a potential risk factor. There are both demographic, behavourial and medical risk factors. Using various classification models, we would try to predict the patient has a risk of suffering from coronary heart disease in the upcoming ten years based on the present conditions of the patient.


<h1> Problem Statement </h1>

The classification goal is to predict whether the patient has a 10-year risk of future coronary disease (CHD).


<h1> Getting to Know the Data </h1>

* Number of Rows and Columns: 3390 rows and 17 columns.
* Number of Duplicate Values: 0 duplicate values.
* Number of Missing/Null Values: 510 duplicate values.


<h1> Understanding The Variables </h1>

 1. **age**: The age of the patient (in discrete numerical values).

 2. **education**: Maybe the education level of the patient (in nominal categorical numbers).
         
 3. **sex**: Whether the patient is male ('M') or female ('F').

 4. **is_smoking**: Whether the patient is smoking currently or not ('YES' or 'NO').

 5. **cigsPerDay**: Number of cigarettes smoked by the patient on an average in a day (discrete numerical values).

 6. **BPMeds**: Whether the patient is taking any medications for blood pressure (nominal categorical numbers: 0 signifying 'No' and 1 signifying 'Yes').

 7. **prevalentStroke**: Whether the patient has a history of stroke (nominal categorical numbers: 0 signifying 'No' and 1 signifying 'Yes').

 8. **prevalentHyp**: Whether the patient has a history of hypertension (nominal categorical numbers: 0 signifying 'No' and 1 signifying 'Yes').

 9. **diabetes**: Whether the patient has diabetes or not (nominal categorical numbers: 0 signifying 'No' and 1 signifying 'Yes').

 10. **totChol**: Measure of the total cholestrol (continuous numerical values).

 11. **sysBP**: Measure of the systolic blood pressure (continuous numerical values).

 12. **diaBP**: Measure of the diastolic blood pressure (continuous numerical values).

 13. **BMI**: The body mass index of the patient (continuous numerical values).

 14. **heartRate**: The heart rate of the the patient (discrete numerical values)

 15. **glucose**: The glucose level of the patient (continuous numerical values).

 16.  **TenYearCHD**: Whether the patient has a 10-year risk of future coronary heart disease (nominal categorical numbers: 0 signifying 'No' and 1 signifying 'Yes').


<h1> Data Wrangling </h1>

The following steps were performed:

* Modifying the column names.
* Taking care of the null values.
* Sanity Checks.
* Separating the independent variables and the dependent variable.

<h1> Hypothesis Testing </h1>
* Chi-Square Test is used to check whether there is relation between the gender of the patient and the risk of developing a coronary heart disease (CHD).
* Chi-Square Test is used to check whether there is relation between the education level of the patient and the risk of developing a coronary heart disease (CHD).

<h1> Feature Engineering & Data Pre-processing </h1>

The following steps were performed:

* Handling the outliers.
* Categorical encoding.
* Feature manipulation.
* Feature selection.
* Data transformation.
* Data scaling.
* Data splitting.
* Handling imbalanced dataset.


<h1> ML Model Implementation </h1>

The following ML Models were implemented:

* Logistic Regression
* Decision Trees
* K-Nearest Neighbors
* Random Forest
* Support Vector Machine
* AdaBoost


<h1> Conclusion </h1>

* All the required data wrangling steps were implemented to take of the null/missing values, separate the dependent variable & independent variables and modify the column names.

* While visualising the data, it was discovered that the dependent vairable is highly imbalanced and a couple of the independent variables were correlated. Also, many details about the categorical columns and the numerical columns were discovered.

* To ensure a better a performance of the models, feature engineering on the dataset was performed where:
 - The outliers in the were handled;
 - Categorical encoding was done on one of the features;
 - A new feature was created, the unnecessary were removed;
 - The skewness in the numerical columns was reduced using log transformation;
 - The numerical columns were scaled using StandardScaler;
 - The dataset was split into training dataset and testing dataset;
 - The imbalance in the dependent variable of the training dataset was taken care of using the SMOTE method.

* The following models were used:
  - Logistic Regression
  - Decision Tree
  - K-Nearest Neighbors
  - Random Forest
  - Support Vector Machine
  - AdaBoost
  along with hyperparameter-tuning.

* After going through the performance metrics of all the implemented model, the Random Forest was chosen as the final prediction model with a Recall score of 0.75 and an ROC-AUC score of 0.88.

* Using SHAP for interpreting the model, it was found that 'pulse_pressure' (a new feature created out of the original 'sysbp' and 'diabp' features), 'age', 'cigsperday' and 'totchol' features had the most impact on the model's output.





