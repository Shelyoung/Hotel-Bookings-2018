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

Then, I moved on to Data Transformation. After taking the steps above, I wanted to structure my data so that is was more readable and organised. The data is there but it's not always in the format that we want or that we need to maximise our analysis. Also, to conduct certain analysis and calculations, it would be useful to add more columns that filter certain info or that gives me a value that the other columns just don't. These are the steps I took:

1. Removed the first 3 letters of the Booking ID which were the same for all of them. Instead of "INN0001", it now read "0001". I used the RIGHT function to remove the first 3 letters from this column. 
2. The day, month and year of arrival were all in different columns so I created another column to add them together as a full date. I used the DATE function for this. I wanted to do some analysis by year, month and date so I didn't delete any of those columns however, the months were categorized by numbers and I needed them in Text so I created another column and used the TEXT function to return only the first 3 letters of the month.
3. Now, I wanted to distinguish arrival dates on weekdays and weekends. For this, I needed to create another column to distinguish these for each booking. I used the Function =IF(WEEKDAY(C6516,2)>5,"Weekend","Weekday"). I also wanted the specific Day of the week as well (i.e Mon, Tue, Wed, etc), so I used the Function =TEXT(A2, "dddd")
4. Under the column Booking Status, the values have an underscore symbol so I removed all of those and replaced it with a space, with the SUBSTITUTE function. I then created an IF function to categorize the Cancelled bookings as 0 and Not cancelled as 1.
5. I used the same RIGHT function as in Step 1 to remove Room_Type and only leave the Room number and to remove Room_Type and only leave the number. I replaced all Not Selected to None using the Find and Replace function. 
6. Now it was time to add a few more columns. I added a column with the duration of stay by adding weekend and weekday nights. I added a Total price column by multiplying the duration of stay by the room price. A column was added to identify a booking as only having Adults or Adults with Children, using the IF(AND) function.
7. I changed some titles to make them more neat.

Once I had my dataset cleaned and prepped, I double checked to see if there any blank values again using the COUNTBLANK function. There were none so it was time to move to the analysis!

This dataset was from a span period between July 2017 and Dec 2018, which means that 2017 had way less data than 2018. I decided to only do the analysis for 2018. There was a total of 36275 bookings for the full dataset, and 29761 for 2018 only. 

![11](https://user-images.githubusercontent.com/122553754/212370829-ef3a1528-d189-47ea-85a8-5d2bfac1c242.PNG)

