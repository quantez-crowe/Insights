# Insights from my Excel project [Diabetes_Dataset](https://github.com/quantez-crowe/Excel_Documents/blob/bf440b6a3868db30e5f92f203c9eaf8914449443/diabetes_dataset_analysis.xlsx)


### Question 1: What is average age of men/women in this dataset, grouped by race/ethnicity? 

![image](https://github.com/user-attachments/assets/d883afce-fd47-4e9c-9511-ce759dba5485)


### Question 2: Create a pivot chart based on BMI classification

![image](https://github.com/user-attachments/assets/5e2f85fb-f09a-4412-b309-8c6ff5ede396)


### Question 3: Create a lookup table that replaces ethnicity codes with their expanded definition (i.e., replace 'W' with 'White', etc.). Create a pivot table with the result. 

1. I created a table (manual) of each of the ethnicity codes and their respective values, and utilized XLOOKUP to return the result:
   
   ![image](https://github.com/user-attachments/assets/6c5049a1-9fc0-44bf-a97f-88478e7a26f4)


   ![image](https://github.com/user-attachments/assets/0e09d0da-4104-486d-9b92-305f06e97880)

(Result)

![image](https://github.com/user-attachments/assets/0a97a0bb-b398-4420-b45f-bf58b801e387)



### Question 4: Use a formula to classify the three results for cholesterol (total, HDL, LDL) into a single string.

1. First, I researched cholesterol levels and learned the cutoffs for each reading. I used data from the [Cleveland Clinic](https://my.clevelandclinic.org/health/articles/11920-cholesterol-numbers-what-do-they-mean) to guide me:

![image](https://github.com/user-attachments/assets/2d720d41-dc4c-45f3-a13c-68912776cc68)

2. For each cholesterol result (total, LDL, HDL), I used the IFS function to classify each reading:

Total Cholesterol: 

![image](https://github.com/user-attachments/assets/faf6d600-315c-4890-95b4-8ba81689c0d7)

HDL:

![image](https://github.com/user-attachments/assets/efe696f8-2574-4ef0-a739-2d7765b211bf)


LDL:

![image](https://github.com/user-attachments/assets/a619a2d1-c1de-4431-8327-84fd4afc0c2a)



Finally, I added a new column, 'Cholesterol Overall', and utilized the CONCAT function to combine these strings into a single reading:

![image](https://github.com/user-attachments/assets/7125b4a1-f949-486b-b4b6-875a02337351)

The final output:

![image](https://github.com/user-attachments/assets/da29b91c-0271-4b6b-9d68-61421787d914)


