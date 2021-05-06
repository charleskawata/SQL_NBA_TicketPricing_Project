# SQL_NBA_TicketPricing_Project

# Project Objective
With Covid-19 restrictions lifting and our country begins to return to normal, NBA teams have to navigate how they are going to bring back fans into arenas and price tickets accordingly. There are many challenges for teams to price tickets which include state mandated capacity limits, hesitancy among fans, and safety. 

I am going to be solving this problem by looking at the remaining games from April 19, 2021 to the end of the 2020-2021 season pulled from the TicketMaster API and historical data on all 30 NBA teams

# Job Description
I was inspired to take on this project because of my love for basketball and a job posting I saw for a Director of Ticket Sales for the Los Angeles Clippers and was interested in exploring the position. The job responsibilities of the role include 
- Provide leadership and establish a positive sales culture for the Ticket Sales department through the hiring, training, coaching and mentorship of all ticketing staff to achieve team established team individual ticketing and related business annual revenue goals.
- Direct Group Sales department through the Group Sales Manager.
- Develop and manage lead campaigns through our CRM system. Ensure maximum utilization of our CRM, other database and ticketing systems to effectively prospect, sell, retain and track results.
- Establish ticket sales strategy, goals and metrics for all Agua Caliente Clippers ticket inventory: season tickets, flex plans, groups and suite; and lead ticket sales team in execution of strategy and to meet sales goals.
- Contribute to revenue goals by selling and managing a book of business, specifically VIP Courtside accounts.
- Produce timely, accurate reporting that monitors the progress of the sales team individually and collectively.
- Supervise all designated gameday ticketing operations including - but not limited to ticketing interns, ticket takers, ticket office, box office, and will-call operations that meets customer service standards established by the team.
- Collaborate with all internal department regarding the overall ticket sales efforts and related team game day functions.
- Establish and provide ongoing review policies and procedures that support the seamless execution of critical initiatives.
- Other duties as the need arises.

I was inspired to take a look at the problem of ticket pricing while I was searching for data to analyze and instead of just looking at ticket pricing for the LA Clippers I decied to look at all of the teams. 

# Data
I got half of my data from the TicketMaster API which I pulled in my `Data_Collection` jupyter notebook and put into the `games` table in my database. The rest of the data came fromdataworld datasets or were manually inputted from these sources 
- https://www.sportico.com/valuations/teams/2021/nba-valuations-data-viz-1234620502/ 
- https://basketball.realgm.com/nba/playoffs/history/1981
- https://finance.yahoo.com/news/average-ticket-prices-nba-team-100000563.html
- https://data.world/gmoney/nba-team-annual-attendance

# Notebooks
The two notebooks are linked above called data_collection and sql_analysis. The first notebook titled data_collection is where I used the TicketMaster API and pulled the necessary data for remaining games for NBA teams. I pulled only the important data points that I needed by looking at the raw JSON and then looped through each record to pull the necessary data. Then I put the data into a data frame which I was allowed to download as a CSV to upload into my database. For the other tables in my database, I manually input the data into Excel files or donwloaded the datasets as Excel files, saved them as CSVs, and then loaded them into my database on hosted on AWS though tablePLus and Dbeaver. The second notebook 'sql_analysis` is where I did my SQL queries to exlpopre the data and then try to answer the primary question of "With the coronavirus how can we evaluate the remaining games for the 2020-2021 NBA season and price the tickets based on stats from each team such as historical attendance, historical ticket prices, historical revenues, and team prestige" 

# Future Improvements
In the future I would try and improve the quality of the data that I had and also create a more reliable and realistic function to help determine ticket prices. With my data sets, some of them did not have up to date information and some of them were missing some key data points that I think could have made analysis more interesting and more accurate. Because other factors influence ticket prices such as day of the week, injuries, supply and demand, time of the game, whether the game is going to be on national television, and team record at the time of the game which would be very helpful in determining ticket prices along with historical data. For my function to determine ticket prices I would want to improve it to include other factors because there are numerous factors that influence ticket prices. 
