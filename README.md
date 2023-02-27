# Analysis of the Hotel Bookings for the year of 2018

You're the hotel owner and you want to find out some interesting things about your Hotel for the year of 2018. What were the busiest ones? How much in advance did people book during those peak months? What is our target market? So many questions to answer... But how? With DATA! 
You know when you book that marvellous room for the week alone, with your partner or family? That is all being recorded in the form of data and it's from there that we can get these amazing insights about the Hotel! So, let's dig in. 

I got this Excel dataset from Kaggle. If you are in data, I am sure you have heard about it. 

https://www.kaggle.com/datasets/ahsan81/hotel-reservations-classification-dataset 

Steps:

1. Data extraction: from Kaggle, I downloaded the dataset and opened it on Excel.
2. Data cleaning: removed unnecessary columns for my specific analysis, changed the data types, removed duplicates, removed rows with missing values (relevant to my analysis), corrected any mispellings. 
3. Data transformation: transformed the data to gain more useful insights. Used several functions (SUMIF, COUNTIF, Nested IF AND, WEEKDAY, TEXT, MONTH, YEAR, DAY, LEFT, LEN, REPLACE)
4. Data Exploration/Analysis: performed data analysis by looking at the distribution of the data and correlations between variables to uncover insights. Performed the aggregation analysis with Pivot Tables and created appropriate visualizations.
5. Data Visualization: create a dashboard with the relevant visualizations and uncover meaningful insights to improve business performance. 

Dashboard

![1a](https://user-images.githubusercontent.com/122553754/221566836-8b3c473d-d5f8-4562-9b74-310c51a05bc7.PNG)


Data Analysis: 

- Bookings steadily increase and remain higher during June-October and decrease after November.
- The month with the highest booking is October with 3381 bookings.
- The main booking source is Online, accounting for 69% of bookings, followed by offline bookings.
- Bookings for the months of June-October are made much in advance than other months.
- Almost a 1/3 of the bookings were cancelled and almost 70% of those cancellations came from customers who made their bookings online.
- The average duration of stay remains quite constant throughout the year, with the average being 3.1 days.
- Bookings are made much more in advance for the months June-October.

Insights/recommendations

- It is possible to detect the hotel's peak season and off-peak season. The peak season is between June-October and off-peak season is November-May.
- It's not surprising that 2/3 of the bookings are made online as we live in a period ruled by the web but most of the cancellations also come from these online bookings. This is an important issue to tackle as revenue is consistenly being affected and one way to do that is: implement a cancellation policy or if there is one in place already, revise it so that the customers are held more accountable in the event of a booking cancellation.
- The average duration of stay is around 3 days but this is something that can be looked at to increase profit. Special discounts/packages can be given to customers who stay for a minimum amount of days. This could increase the hotel's brand awarenned, average duration of stay and, subsequently, the profit. These discounts should be mostly directed to online bookings with the goal to also reduce cancellations.

It would also be interesting to analyse when did these cancellations occur to spot any trends, i.e do cancellations occur closer to the booking date or weeks before?




