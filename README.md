# data-collection---challenge
Module 11 - Data collection challenge

**BACKGROUND**

With this challenge, I continued to strengthen my core data analytics skills: collecting data, organizing and storing data, analyzing data, and visually communicating my insights.

**DELIVERABLE AND ASSOCIATED REQUIREMENTS**

**1. Scraped Titles and Previewed Text from Mars News**

a. Used automated browsing to visit the [Mars news site](https://static.bc-edx.com/data/web/mars_news/index.html).

b. Created a Beautiful Soup object and used it to extract text elements from the website.

c. Extracted the titles and previewed text of the news articles scraped. 
* Stored each title-and-preview pair in a Python dictionary and gave each dictionary two keys: title and preview.
* Stored all the dictionaries in a Python list.
* Printed the list in my [Jupyter notebook](https://github.com/rperez025/data-collection---challenge/blob/main/part_1_mars_news.ipynb).

d. Stored the scraped data in a file to ease sharing the data with others - exported the scraped data to a JSON file.

**2. Scraped and Analyzed Mars Weather Data**

a. Used automated browsing to visit the [Mars Temperature Data Site](https://static.bc-edx.com/data/web/mars_facts/temperature.html).

b. Created a Beautiful Soup object and used it to scrape the data in the HTML table. 

c. Assembled the scraped data into a Pandas DataFrame. Ensured the columns should have the following column headings:
* id: the identification number of a single transmission from the Curiosity rover
* terrestrial_date: the date on Earth
* sol: the number of elapsed sols (Martian days) since Curiosity landed on Mars
* ls: the solar longitude
* month: the Martian month
* min_temp: the minimum temperature, in Celsius, of a single Martian day (sol)
* pressure: The atmospheric pressure at Curiosity's location

d. Examined the data types that are currently associated with each column and casted (or converted) the data to the appropriate datetime, int, or float data types.

e. Analyzed the dataset by using Pandas functions to answer the following questions:
* How many months exist on Mars?
* How many Martian (and not Earth) days worth of data exist in the scraped dataset?
* What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
  - Find the average minimum daily temperature for all of the months.
  - Plot the results as a bar chart.
* Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
  - Find the average daily atmospheric pressure of all the months.
  - Plot the results as a bar chart.
* About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
  - Consider how many days elapse on Earth in the time that Mars circles the Sun once.
  - Visually estimate the result by plotting the daily minimum temperature.

f. Exported the DataFrame to a CSV file.

**RESOURCES AND REFERENCES**

During the challenge, I referenced the following to aid in my understanding and completion of the assignment:

1. Reviewed and reperformed a majority of the class activities in my GitLab Working Folder.

2. Watched the following instructor videos made by Dr. A:
* [SQL Day 03 - Activities 10 and 11 - (Demo)](https://www.youtube.com/watch?v=npftGEiTsaY)
* [SQL Alchemy Day 01 - Activity 11 - Surfer SQL (Demo)](https://www.youtube.com/watch?v=vNu18haZWGE)
* [SQL Alchemy Day 02 - Activity 08 - Salary Exploration (Extended Demo)](https://www.youtube.com/watch?v=liui4_Ukp6k)
* [SQL Alchemy Day 02 - Activity 04 - Travel DB with CRUD (Extended Demo)](https://www.youtube.com/watch?v=pKUYb2qq7z4)
* [SQL Alchemy Day 03 - Activity 7, 8, & 9 Walkthrough](https://www.youtube.com/watch?v=Tj4A8vHS7hM)
* [SQL Alchemy Day 03 - Activity 11 Solution](https://www.youtube.com/watch?v=y8C_NuCo_7o)

3. Research reference:
- [Change the data type of a column or a Pandas Series](https://www.geeksforgeeks.org/change-the-data-type-of-a-column-or-a-pandas-series/)

4. Code reference:
* In [8] convert_dict={'id':int,'sol':int,'ls':int,'month':int,'min_temp':float,'pressure':float}temp_df=temp_df.astype(convert_dict)temp_df["terrestrial_date"]=pd.to_datetime(temp_df["terrestrial_date"])print(temp_df.dtypes) -- Used in [part_2_mars_weather.ipynb](https://github.com/rperez025/data-collection---challenge/blob/main/part_2_mars_weather.ipynb) in In [10]
