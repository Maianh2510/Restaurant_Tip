# **🍽️ Restaurant Tips Analysis**

![image](https://github.com/user-attachments/assets/0433addc-1d29-4ca5-aa79-9542ec975435)

This project aims to use the restaurant tips dataset to practice creating composition plots and visualizations. We will examine the relationship between different variables and the tips given.

The dataset consists of information from 244 restaurant bills, collected in the US in 1987.

It includes details about the tips given to restaurant staff, such as the total bill, tip amount, gender of the person paying, smoking status, day of the week, time of day, and party size.

**Data details**

**Source:** Swiss coding academy

**The main goal of this analysis:**
We will learn more the relationship between different variables and the tips given

**We need to answers below to find main goal:**
1. What is the data like?
2. What does the data need to clean?
3. What does the data group customer by?
4. What does the data need to calculate?
6. How do we need to compare groups by criteria?

**How do we do to answer?**

What is the data like?
   1. Import pandas ,matplotlib
   2. Read and Check data
   Results as :                      
*    The day it occurred
*    If it was at lunch or dinner
*    The total bill
*    The sex of the person
*    If they were a smoker or not
*    The size of the party
You can see table 5 first row of data :

||Id|Total_bill|Tip|Sex|Smoker|	Day|Time|Size|
|---|---|---|---|---|---|---|---|---|
|0|0|16.99|1.01|Female|No|Sun|	Dinner|	2|
|1|1|10.34|1.66|Male|No|Sun|	Dinner|	3|
|2|2|21.01|3.50|Male|No|Sun|	Dinner|	3|
|3|3|23.68|3.31|Male|No|Sun|	Dinner|	2|
|4|4|24.59|3.61|Female|No|Sun|	Dinner|	4|

What does the data need to clean?
   1. Check values is null, Check values is duplicate. Results: they are fine
   2. Check typyes and We have string columns considered as objects. So we fix their types correct.

      Result: We have dtypes: Float64(2), Int64(2), string(4). They fixed correct.

What does the data group customer by?

We need to calculate the tip figures between the two customer files. And we categorize the datas to be compared as follows:
* Smokers and non-smokers
* Male and Female
* Weekends and weekdays
* Lunch and dinner ( *We checked data about column time, and the result is the restaurant only has 2 service times*)

What does the data need to calculate?
  1. View describe data
  2. Calculate the metrics for the customer groups listed above as: Min, Max, Mean, Median

How do we need to compare groups by criteria?
We use T-test to compare groups by criteria. And we use matplotlib to distribution comparison. 

You can see how I do them in detail here: https://colab.research.google.com/drive/1ZyT3H1C8TqUXtE99oqKlXoY_WLR1vGZl?usp=sharing

### **📝 SUMMARY**

After We have results. We have some Insights and conclussion as :

### **The First: smokers and non-smokers**

![image](https://github.com/user-attachments/assets/308d6d8f-4553-43bc-a8e2-5926f79e5209)

###### Insights based on measures of central tendency comparison:
1. Smokers include higher tip values (up to 10.0), whereas non-smokers' maximum tip is slightly lower (9.0).
2. This contributes to the higher mean and median for smokers.
   
##### General conclusion:

Smokers tip slightly higher on average (mean) and also have a higher central value (median) compared to non-smokers.
Smokers also show a wider range, with tips reaching up to 10 units, whereas non-smokers' tips are capped at 9 units.
This confirms that smokers tend to tip more generously overall.

##### General conclusion: The smokers usually give tip higher non-smokers

![image](https://github.com/user-attachments/assets/6883d4f7-b4aa-42c8-9da7-40442d6a0361)

###### Insights based on distribution comparison:
1. Smokers tend to tip higher than non-smokers, as evidenced by the more frequent occurrence of tips in the 6–10 range.
2. Non-smokers, while tipping more frequently in the 1–4 range, contribute far fewer high-value tips.

##### General conclusion:

The data suggests that smokers tip more generously (higher tip values), while non-smokers' tips are smaller and more consistent.

### **The second: Female and male**

![image](https://github.com/user-attachments/assets/a920b618-beb7-4270-9958-711a97ef8781)

###### Insights based on measures of central tendency comparison:
1. The Female group has the smallest range (from 1 to 6.5), whereas the Male and Common groups span from 1 to 10.
2. The Male group tends to have slightly higher averages and medians compared to Female.

##### General conclusion: The male usually give tip higher female

![image](https://github.com/user-attachments/assets/9da4fd16-8dc2-4117-bfeb-940304e7a965)

###### Insights based on distribution comparison:
1. Both genders primarily tip smaller amounts (1–4).
2. Males have a slightly wider range of tip values and more to tip higher amounts than females.

##### General conclusion:

The overall dataset reflects this trend, as male tips dominate the higher values in the data.

### **The third: Weekends and Weekdays**

![image](https://github.com/user-attachments/assets/406ec05a-6625-4050-b026-1fbfa9f45a07)

###### Insights based on measures of central tendency comparison:
1. The mean score for Weekends is 3.115, which is higher than the mean for Weekdays (2.735). This suggests better or higher outcomes on weekends compared to weekdays.
2. Weekdays have a maximum value of 4.73, which is much lower than Common and Weekend values, both of which reach up to 10.

##### General conclusion:The weekends usually give tip higher weekdays

![image](https://github.com/user-attachments/assets/644b0257-096d-4b4a-85f2-6f96919b77e1)

###### Insights based on distribution comparison:
1. Tip amounts are generally higher on weekends compared to weekdays, both in frequency and magnitude.
2. On weekdays, tips are more concentrated within a smaller range (around 1 USD to 4.5 USD).

###### General conclusion:

The entire dataset shows that tips rarely exceed 6 USD, confirming that low-to-mid tips are the most common behavior.

### **The last: Dinner and lunch**

![image](https://github.com/user-attachments/assets/77a66cfc-69d0-4322-afcb-c7e561baab40)

###### Insights based on measures of central tendency comparison:
1. Minimum Tip: The minimum tip is slightly higher for lunch (1.25) compared to dinner (1.00), indicating that even the lowest tips during lunch are slightly larger.
2. Maximum Tip: The maximum tip for dinner reaches 10.0, which is notably higher than lunch (6.7). This suggests that larger tips are more likely to occur during dinner.

###### General conclusion: The dinner usually give tip higher lunch

![image](https://github.com/user-attachments/assets/906982ec-c192-46fe-8504-af2787e31344)

###### Insights based on distribution comparison:
1. Dinner tips are generally larger and more variable compared to lunch tips. Higher tips above 6USD occur more frequently at dinner whereas lunch tips rarely exceed 4USD to 5USD.
2. Lunch tips are more modest, concentrated in the lower range (1USD to 3USD), with fewer outliers or high tips.

###### General conclusion:

The overall dataset reflects this trend, as dinner tips dominate the higher values in the combined data.

## **📝 CONCLUSION**     

###### **After processing and calculating the data, we have the highlights:**

* The smokers tip more than non-smokers
* The male tip more than female
* The weekends have tip more than weekdays
* The dinner group have tip more than lunch group

You can see how I do them in detail here: https://colab.research.google.com/drive/1SSCkl12zRgoFeqvvyyIQbCSMXOpyFqfs?usp=sharing

**However, there aren't any much difference between the relationship variables and the tips given.**
