# Webscraping
MARS DATA SCRAPING AND ANALYSIS


# 1.Introduction:

Embarking on Mars data exploration, i'll scrape mars news('https://static.bc-edx.com/data/web/mars_news/index.html') and weather details(https://static.bc-edx.com/data/web/mars_facts/temperature.html) urls. From it, i'll extract:
a: Scrape titles and preview text from Mars news articles.
 b: Scrape and analyze Mars weather data, which exists in a table.

# 2.Finding:

Stored each title-and-preview pair in a Python dictionary and, gave each dictionary two keys: title and preview. An example is the following:

{'title': "NASA's MAVEN Observes Martian Light Show Caused by Major Solar Storm",
 'preview': "For the first time in its eight years orbiting Mars, NASA’s MAVEN mission witnessed two different types of ultraviolet aurorae simultaneously, the result of solar storms that began on Aug. 27."}


Store all the dictionaries in a Python list.

 and Print the list in your notebook.

 For Weather details:

 1. I scraped the table to get the data for the rows:
# Extract all rows of data
all_rows= soup.find_all('tr', class_='data-row')
all_rows

2. Stored the scarped data in a list format to create a list of rows:

3. Created a panda DataFrame using the list of rows and column names:

# 3.From the dataFrame : the Analysis part came:


i. How many months exist on Mars?
-used the .nunique() method to find that we have 12 months in Mars.


ii. How many Martian (and not Earth) days worth of data exist in the scraped dataset?
-used [sol]column to count how many martian days of data exist= 1867 days


iii. What are the coldest and the warmest months on Mars (at the location of Curiosity)? To answer this question:
    * Find the average the minimum daily temperature for all of the months.
    * Plot the results as a bar chart.

- used the groupby method to group the month and use the mean method ot average the min_temp

iv. Which months have the lowest and the highest atmospheric pressure on Mars? To answer this question:
    * Find the average the daily atmospheric pressure of all the months.
    * Plot the results as a bar chart.

-- used the groupby method to group the month and use the mean method ot average the pressure
--plot using bar graph

v. About how many terrestrial (Earth) days exist in a Martian year? To answer this question:
    * Consider how many days elapse on Earth in the time that Mars circles the Sun once.
    * Visually estimate the result by plotting the daily minimum temperature.
-- by analysing the Martain year duration, we've determined that a year on Mars is roughlt 675 days compared to the 365 days of Earth, thus showcasing Mars distinct orbit around the sun and emphasisng it is longer seasonal cycle.

# 4.Conclusion
The profound difference between Earth and Mars climate is evident between the two planets. Mars extreme cold temperature is uniquely different from Earth's.
The project demonstarted the ability to effectively use web scraping techniques to collect and analyze data from a Mars-related Website, providing valuable insight to Martian months, pressure, temperature and days.



