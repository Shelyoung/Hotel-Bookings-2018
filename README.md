# Analysis of the Hotel Bookings for the year of 2018

You're the hotel owner and you want to find out some interesting things about your Hotel for the year of 2018. What were the busiest ones? How much in advance did people book during those peak months? What is our target market? So many questions to answer... But how? With DATA! 
You know when you book that marvellous room for the week alone, with your partner or family? That is all being recorded in the form of data and it's from there that we can get these amazing insights about the Hotel! So, let's dig in. 

First, data extraction. I got this Excel dataset from Kaggle. If you are in data, I am sure you have heard about it. 

https://www.kaggle.com/datasets/ahsan81/hotel-reservations-classification-dataset 

Next, it's one the most (if not the most) important part of the Data Analysis cycle: Data preparation. This includes finding any erros, duplicates, irrevelant info or columns and scraping them, transforming your data into a certain format or structure. We don't dirty data, we want data that is accurate and that is useful to what we are trying to achieve. 

Starting off with Data Cleansing, these are the steps I took:

1. I removed all columns that were irrelevant for my analysis, especially the ones that had only zeros. They weren't useful so there wasn't any point in taking up extra space. 
2. I checked for any possible duplicates (i.e duplicate Booking IDs) through the conditional formatting since this would provide innacurate analysis.
3. Made sure that the columns followed the same capitalization. We don't want our data looking messy with some columns in Caps Lock and others in lower case.
4. Changed the column's data types to the correct ones. Some categorical columns were set as numerical and vice versa. This step is crucial to conduct calculations later on. 
5. Did a quick spell check in the categorical columns. For example, Meal Type is supposed to only have 4 values (3 different meal types or none selected). A value might be mispelled as Meal Tpe 3, which would another incorrect value to this column. 

Then, I moved on to Data Transformation. After taking the steps above, I wanted to structure my data so that is was more readable and organised. The data is there but it's not always in the format that we want or that we need to maximise our analysis. Also, to conduct certain analysis and calculations, it would be useful to add more columns that filter certain info or that gives me a value that the other columns just don't. 
