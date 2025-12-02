📊 Netflix Content Analysis – Power BI Dashboard
📌 Project Overview

This Power BI dashboard provides an interactive analysis of Netflix Movies & TV Shows.
The goal of this project is to explore how Netflix content is distributed across years, ratings, countries, content types, and directors, and convert raw data into meaningful insights.

🎯 Key Features

KPI Cards – Total Titles, Total Movies, Total TV Shows

Movies vs TV Shows Comparison

Year-wise Content Release Trend

Rating Category Breakdown (TV-MA, TV-14, TV-PG, etc.)

Directors Count by Content Type

Country-wise Content Distribution using Map visual

Interactive Filters – Type | Release Year | Country

💡 Insights Derived

Content releases on Netflix increased significantly after 2015

Movies dominate the platform, but TV Shows are growing steadily

Most frequent rating categories are TV-MA, TV-14, and TV-PG

Countries with the highest number of titles include USA, India, UK, and Canada

🛠 Tools & Technologies Used

Power BI (Dashboard creation)

DAX (Measures & KPIs)

Excel/CSV (Data cleaning)

Data Visualization techniques

🧮 DAX Measures
Total Titles = FORMAT(CALCULATE(DISTINCTCOUNT(netflix_titles[show_id])), "#,##0")

Total Movies = FORMAT(
    CALCULATE(DISTINCTCOUNT(netflix_titles[show_id]),
    FILTER(netflix_titles, netflix_titles[type] = "Movie")),
"#,##0"
)

Total TV Shows = FORMAT(
    CALCULATE(DISTINCTCOUNT(netflix_titles[show_id]),
    FILTER(netflix_titles, netflix_titles[type] = "TV Show")),
"#,##0"
)
