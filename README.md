🏡 Airbnb NYC Power BI Analysis Report
-----------------------------------------------
A major portfolio project analysing Airbnb listings in New York City using Power BI. This project covers importing, cleaning, visualizing, and interpreting key insights from the dataset to highlight patterns in room types, neighbourhood performance, and revenue trends.

 📊 Project Summary
----------------------------------------------
Dataset: NYC Airbnb Open Data
Source: Kaggle Dataset
Tool Used: Power BI
Focus Areas: Market overview, revenue insights, neighbourhood patterns
Report Pages:
1. Overview
2. Revenue Insights
3. Neighbourhood Insights

🧹 Data Preparation & Preprocessing
-------------------------------------------------
The original dataset contained several inconsistencies and missing values that required cleaning to ensure accurate analysis. First, rows containing errors in critical columns such as id, host_id, longitude, number_of_reviews, and last_review were identified. Removing error rows from the id column automatically resolved the remaining errors in other columns. Next, missing values in the host_id column were carefully inspected and removed, considering the importance of host identification in Airbnb listings. The last_review and reviews_per_month columns had about 4% missing data, which were imputed with default values. For last_review, missing entries were filled with a default old date (1990-01-01) to preserve the datetime format without affecting timeline-based analysis. New calculated columns were added to enrich the dataset, such as demand_flag (high demand area based on number of reviews), recently_reviewed (filtering listings with “Yes” or “No” based on active engagement) , price_per_night (shows how much it costs per night) and a rounded version of the price column using the Number.Round() function in Power Query to remove decimal places. Listings with extreme values (e.g., unrealistic prices above $1000 per night or minimum nights greater than 365) were filtered out, as they skewed the distribution and could distort visual insights. This helped maintain focus on typical listings and improved the reliability of the visual analysis. Overall, preprocessing ensured a clean, consistent, and analysis-ready dataset.


📌 Report Structure & Visuals
-----------------------------------------------------
1️⃣ Overview Page
Provides a snapshot of Airbnb activity in NYC.
* Cards showing:
1. Total Listings
2. Total reviews
3. Average Price
4. Most Common Room Type
5. Most popular Neighbourhood
* Column Chart: Distribution of Room Types across NYC
* Map showing locations of listings around New York
* Buttons: Navigation to Revenue & Neighbourhood Insights
* Other visuals

2️⃣ Revenue Insights
Explores revenue generation and pricing behavior.
Cards: Total revenue and average revenue per listing
Slicers: Room type and neighbourhood group
Bar chart: Top 5 hosts by revenue
Bar chart: Total revenue by room type
Clustered column chart: Total revenue by Neighbourhood Group and room type
Area chart: Total revenue by year

3️⃣ Neighbourhood Insights
This page provides a focused analysis of price variations across neighbourhoods and room types in NYC, helping uncover which localities are the most active and profitable on Airbnb.
1. KPI Cards: Total neighbourhood, Total neighbourhood by listings, Total neighbourhood by revenue
2. Matrix Table: Average price by neighbourhood and room type
3. Slicers: Room type and neighbourhood group

🖼️ Design & Interactivity
--------------------------------------------------------------
1. Navigation Buttons for seamless switching between pages
2. Bookmarks to highlight filtered views
3. Images and Icons used for branding and better UX (Airbnb logo, NYC map)
4. Consistent color scheme and clean layout for ease of interpretation

💡 Key Insights & Takeaways
-----------------------------------------------------------------
📌 Market Trends
1. Manhattan dominates the market in both listing count and revenue generation.
2. Entire home/apartment is the most preferred room type by hosts and guests.
3. Brooklyn and Queens also host a large volume of listings but tend to have lower average prices compared to Manhattan.

💸 Revenue Behavior
1. Listings with moderate pricing (~$100–200) tend to receive the most reviews, suggesting a sweet spot for both demand and value.
2. A small number of high-performing neighbourhoods account for a large share of total revenue.
3. Superhosts or listings with high reviews often cluster around tourist hotspots.

📍 Spatial Distribution
1. Listing density is highest in areas like Lower Manhattan, Williamsburg, and Midtown.
2. Peripheral boroughs like the Bronx and Staten Island have fewer listings with lower review counts.
3. Locations close to central transit or attractions perform better in both price and review volume.

📁 Files Included
----------------------------------------------------------
1. AirBnB-Analysis.pbix: Power BI report file
2. README.md: Project documentation

📌 Final Thoughts
----------------------------------------
This dashboard helps stakeholders—such as hosts, travelers, or Airbnb analysts—understand where to focus their attention for better pricing, marketing, or investment decisions. It also demonstrates proficiency in Power BI for data wrangling, analysis, and visual storytelling.
