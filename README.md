# codealpha_tasks
My CodeAlpha internship tasks and projects.
CodeAlpha_EDA

Exploratory data analysis and an interactive dashboard on a Netflix user dataset. Task 2 (Exploratory Data Analysis) of the CodeAlpha Data Analytics Internship.

Objective

Understand who Netflix users are, what they watch, and whether plan type, age or country changes how much they watch.

Dataset

netflix.csv: 25,000 users, 8 columns.

Column	Description
User_ID	Unique user number
Name	User name
Age	13 to 80
Country	10 countries
Subscription_Type	Basic, Standard, Premium
Watch_Time_Hours	Total hours watched
Favorite_Genre	7 genres
Last_Login	Last login date (8 Mar 2024 to 8 Mar 2025)
Questions I asked
How are users split across subscription types?
Which countries have the most users?
Which genres are the most popular?
What is the age profile of users?
How much do users watch, and are there outliers?
Does subscription type affect watch time?
Does age affect watch time?
Does favourite genre differ across age groups?
How do last-login dates spread over the year?
Hypotheses: Premium users watch more than Basic users; age and watch time are correlated.
What I did
Data checks: no missing values, no duplicate rows, User_ID unique, no impossible values.
Cleaning: converted Last_Login from text to a date; created age_group, login_month and days_since_login.
Analysis: counts and distributions, group comparisons, IQR outlier check, correlation, genre by age group.
Statistical tests: Welch t-test, one-way ANOVA, Pearson correlation, chi-square.
Dashboard: interactive HTML page with filters for plan, country, age group and genre.
Key findings
Plans are evenly split: Premium 33.6%, Basic 33.4%, Standard 33.0%.
Countries: UK has the most users (2,592) and Australia the fewest (2,437). The spread across the 10 countries is small.
Genres: Horror is most popular (3,654 users) and Sci-Fi least (3,455).
Age: users range from 13 to 80, with a mean of 46.5 and a median of 46.
Watch time: mean 500.5 hours, median 501.5 hours, spread evenly from about 0 to 1,000 hours. The IQR method finds no outliers.
Plan vs watch time: Basic 503.0 h, Standard 496.9 h, Premium 501.4 h. No significant difference (ANOVA p = 0.37; Premium vs Basic p = 0.64).
Age vs watch time: correlation r = 0.008 (p = 0.21), so there is no relationship.
Genre vs plan: no dependence (chi-square p = 0.20).

Overall: no plan, country, age group or genre stands out. Users are spread almost evenly, so none of the segments I checked would be a useful way to target or separate users.
Dashboard

Open dashboard.html in a browser.

Filters: plan, country, age group, favourite genre
Key numbers: users, average and median watch time, average age, top genre
Charts: subscription split, watch time by plan and age group, users by country, genre and age group, watch time distribution, last-login months, genre-by-age heatmap
Test results panel from the notebook


Limitations
The dataset has only 8 columns, with no device, price, content titles or cancellation data.
Last_Login is one date per user, so it shows when users last logged in, not activity over time.
Names repeat (100 unique names across 25,000 users), so Name was not used.

Tools

Python, pandas, NumPy, Matplotlib, Seaborn, SciPy, HTML, CSS, JavaScript
