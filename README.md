This project is part of my Data Analyst Internship, where I cleaned and preprocessed a raw dataset using Python (Pandas) in Google Colab.
The dataset used is the Medical Appointments No-Show Dataset, publicly available on Mendeley Data:

🔗 Dataset Link: https://data.mendeley.com/datasets/wm6w2fvkfj/1

The goal of this task was to clean the dataset by fixing missing values, duplicates, inconsistent formats, incorrect data types, and preparing it for analysis.

🛠 Tools & Technologies

Python

Pandas

Google Colab

📁 Files Included

cleaned_medical_appointments.csv

medical-appointments-no-show.csv

Data_Cleaning_and_Preprocessing.ipynb

README.md

✅ Data Cleaning Steps Performed

1️⃣ Loaded the Dataset

Imported the raw CSV file and inspected its structure.

2️⃣ Missing Values Handling

Checked missing values using:

df.isnull().sum()


Removed rows containing nulls using:

df.dropna()


✔ Final dataset contains 0 missing values.

3️⃣ Duplicate Removal

Checked duplicates using:

df.duplicated().sum()


No duplicate rows were found.

4️⃣ Column Name Standardization

All column names were cleaned by:

converting to lowercase

replacing spaces with underscores

replacing hyphens with underscores

Example:
Entry Service Date → entry_service_date

5️⃣ Date Format Conversion

Attempted conversion of all columns containing the word "day":

pd.to_datetime(df[col], errors='coerce')


Invalid conversions were handled safely using errors='coerce'.

6️⃣ Fixed Data Types

Converted valid date columns to datetime

Ensured numeric columns had proper types

Cleaned inconsistent text formatting

7️⃣ Outlier Check

Used the IQR method to find extreme values in numeric fields.

8️⃣ Exported Clean Dataset

Final cleaned dataset saved as:

cleaned_medical_appointments.csv


💡 Key Learnings

Identifying and handling missing and duplicate values

Cleaning inconsistent text and date formats

Ensuring correct data types

Exporting a clean, analysis-ready dataset

Working with real-world messy data
