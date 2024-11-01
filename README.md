# Airbnb Data Analysis Project

## Project Overview
This project is a comprehensive analysis of Airbnb listings, focused on exploring factors that influence pricing and availability. Using a dataset of listings, the project aims to clean, process, and analyze the data to extract insights that can inform pricing strategies, understand market dynamics, and improve decision-making for Airbnb hosts and analysts.

## Dataset
The dataset includes various attributes for each listing, such as:
- **listing_id**: Unique identifier for each listing
- **host_name**: Name of the host
- **last_review**: Date of the last review
- **description**: Description of the listing
- **room_type**: Type of room (e.g., Entire home/apt, Private room, Shared room)
- **price**: Price per night in USD
- **nbhood_full**: Neighborhood and borough information

### Dataset Cleaning Process
1. **Handling Missing Values**:
   - `host_name` and `description` had a few missing values. We filled these with placeholder values ("Unknown") for `host_name` and an empty string for `description`, as these fields were not critical to numerical analysis.

2. **Data Type Corrections**:
   - Converted the `price` column to an integer by removing the "dollars" string and ensuring all values were in USD.
   - Transformed the `last_review` column from an object to a datetime format.

3. **Duplicate Removal**:
   - Checked for and removed duplicate entries to avoid redundant data.

4. **Outlier Detection and Removal**:
   - Detected significant outliers in the `price` column, particularly among shared room listings. After analyzing shared rooms within the same neighborhoods, we identified two listings with extreme prices ($350 and $800) and removed them to maintain data consistency.

## Exploratory Data Analysis (EDA)
After data cleaning, the following steps were performed in EDA to gain insights:

1. **Price Distribution Analysis**:
   - Examined the distribution of prices across different room types and neighborhoods. Created visualizations such as histograms and box plots to identify general trends and patterns.

2. **Room Type Analysis**:
   - Compared price ranges across different room types (e.g., Entire home/apt, Private room, Shared room). This helped understand how room type impacts pricing within specific neighborhoods.

3. **Neighborhood Analysis**:
   - Analyzed the distribution of listings by neighborhood and borough to see which areas have the highest density of listings and how pricing varies by location.

4. **Seasonal Trends**:
   - By analyzing the `last_review` column, we explored how listing activity and review frequency vary over time, which could indicate seasonal demand patterns.

## Key Findings
1. **Price Variability by Room Type**:
   - Entire homes/apartments generally have higher prices than private or shared rooms, as expected.

2. **Outlier Listings**:
   - Some listings had prices significantly above the typical range for their room type and neighborhood. Removing these outliers allowed us to analyze pricing patterns more reliably.

3. **Neighborhood Influence**:
   - Neighborhoods in central Manhattan had notably higher average prices compared to other areas, highlighting the importance of location in pricing.

## Tools and Technologies Used
- **Python**: Data cleaning, analysis, and visualization.
- **Pandas**: Data manipulation and analysis.
- **Matplotlib & Seaborn**: Data visualization.

## Future Improvements
1. **Advanced Feature Engineering**:
   - Add more features such as amenities, proximity to landmarks, and review scores to improve analysis accuracy.

2. **Price Prediction Model**:
   - Develop a predictive model to estimate listing prices based on room type, location, and other features.
