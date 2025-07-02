## Medical-Appointment-No-Show-Dataset-Analysis
This repo contains notebooks on various datasets as a practice on data analysis, all notebooks include:  Data Cleaning. Data Visualization. Exploratory Data Analysis.

# Medical Appointment No Show Dataset Analysis
## Contents
Dataset Description

Columns Descreption

EDA Questions

Data Wrangling

Data Cleaning

Data Visualization

Conclusion

Built with


## Dataset Description:
A person makes a doctor appointment, receives all the instructions and no-show. Who to blame? This dataset collects information from 100k medical appointments in Brazil and is focused on the question of whether or not patients show up for their appointment. A number of characteristics about the patient are included in each row.

## Columns Descreption:

PatientId: Identification of a patient.

AppointmentID: Identification of each appointment.

Gender: Male or Female.

AppointmentDay: The day of the actuall appointment, when they have to visit the doctor.

ScheduledDay: The day someone called or registered the appointment, this is before appointment of course.

Age: How old is the patient.

Neighbourhood: Where the appointment takes place.

Scholarship: True of False. Observation, this is a broad topic, consider reading this article https://en.wikipedia.org/wiki/Bolsa_Fam%C3%ADlia

Hipertension: True or False.

Diabetes: True or False.

Alcoholism: True or False.

Handcap: True or False.

SMS_received: 1 or more messages sent to the patient.

No-show: True or False.

## EDA Questions:

Q1: How often do men go to hospitals compared to women? Which of them is more likely to show up?

Q2: Does recieving an SMS as a reminder affect whether or not a patient may show up? is it correlated with number of days before the appointment?

Q3: Does having a scholarship affects showing up on a hospital appointment? What are the age groups affected by this?

Q4: Does having certain deseases affect whather or not a patient may show up to their appointment? is it affected by gender?


## Data Wrangling:
Our data can be found on noshowappointments-kagglev2-may-2016.csv file provided on this repository, downloaded from Kaggle.

## Data Cleaning:
### Exploration Summery
our dataset consists of 110527 rows with 14 columns, and has no NaNs nor duplicated values.

PatientId and AppointmentId columns wouldn't be helpful during analysis.

ScheduledDay and AppointmentDay needs to be casted to date data type.

we may append a new column for days until appointment.

Gender needs to be casted into a categoy type

Scholarship, Hipertension, Diabetes, Alcoholism and SMS_recieved better be boolean data type.

No-show column needs to be parsed and asted to boolean type.

Handcap colume needs to be cleaned to have only 0 and 1 values.

Age columns has inconsistant unique values that needs to be handled.

We endded up with a datafram of 110521 rows and 11 columns after completing the cleaning process.

## Data Visualization
Using Matplotlib and Seaborn, we made several meaningful visuals and charts to help us gain informative insights regarding any correlation between attributes in our dataset, that'll be discussed in the next section.

## Conclusion
These are derived conclusions after completing our data visualisation phase.

## Q1: How often do men go to hospitals compared to women? Which of them is more likely to show up?

Nearly half of our dataset conists of women with wider age destribution and some outliers, all of which achiees a rate higher than men.
It is obvious that 79.8% of our patients did show up on their appointments and only 20.1% of them did not.
Women do show up on their appointments more often than men do, but this may b affected by the percentage of women on this dataset.

## Q2: Does recieving an SMS as a reminder affect whether or not a patient may show up? is it correlated with number of days before the appointment?

67.8% of our patients did not reciee any SMS reminder of their appointments, yet they showed up on their appointments.
It is clear that there is a positive correlation between number of due days and whether a patient shows up or not.
Patient with appointments from 0 to 30 days tend to show up more regularly, while patients with higher number of days tend to not show up.
gender does not affect number of due days and showing up at an appointment that much.

## Q3: Does having a scholarship affects showing up on a hospital appointment? What are the age groups affected by this?

Having a scholarship does not affect showing up to a doctor appointment that much.
Huge age group is enrolled to that scholarship and also enrol their babies on.

## Q4: Does having certain deseases affect whather or not a patient may show up to their appointment? is it affected by gender?

We can conclude that the vast majority of our dataset does not have chronic deseases, yet, they are existed in so many young people.
Having a chronic deseas may affect your showing up at a hospital's appointment.

## Built with:
JupyterLab

Python3

Pandas

Numpy

Matplotlib

Seaborn
