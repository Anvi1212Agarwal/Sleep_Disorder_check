# Sleep_Disorder_check
💤 Sleep Disorder Prediction

This project builds a machine learning model to predict sleep disorders (such as Sleep Apnea or Insomnia) based on lifestyle, health, and activity data.

📌 Dataset

The dataset contains 374 records with the following features:

Column	Description
Person ID	Unique identifier (removed for training)
Gender	Male / Female
Age	Age in years
Occupation	Profession of the individual
Sleep Duration	Average sleep hours
Quality of Sleep	Sleep quality score (1–10)
Physical Activity Level	Daily activity level
Stress Level	Stress score (1–10)
BMI Category	Underweight / Normal / Overweight / Obese
Blood Pressure	BP value (e.g., 126/83 → converted to average)
Heart Rate	Resting heart rate
Daily Steps	Average daily step count
Sleep Disorder	Target variable (Sleep Apnea, Insomnia, or NaN for missing)

Total Rows: 374

Labeled Sleep Disorder: 155

Unlabeled Sleep Disorder: 219

⚙️ Approach

Data Preprocessing

Removed Person ID (not useful for prediction).

Encoded categorical variables (Gender, Occupation, BMI Category).

Converted Blood Pressure into a numeric average.

Handled missing labels (NaN in Sleep Disorder).

Model Training

Trained a Random Forest Classifier using labeled rows (155 samples).

Features were standardized with StandardScaler.

Evaluated model performance with accuracy, classification report, and confusion matrix.

Prediction of Missing Labels

Used the trained model to predict missing Sleep Disorder values (219 samples).

Produced a complete dataset with all 374 rows labeled.

🛠️ Tech Stack

Python 3

pandas, numpy → Data processing

scikit-learn → ML model, preprocessing, evaluation

RandomForestClassifier → Baseline predictive model

📊 Example Results

Training Accuracy: ~100% (RF fits well on small dataset)

Test Accuracy: ~85–90% (varies by split)

Key features affecting prediction:

Sleep Duration

Stress Level

BMI Category

Blood Pressure
