# Advanced Spreadsheets: Project

## Introduction

You’ve been hired by a consulting company to analyze the vacation rental market in Manhattan, New York City, using data from Airbnb listings. Your task is to provide insights to help the client prioritize investment opportunities in the vacation rental market.

## Part 1 - Explore and filter the data

### Prepare tabs for documentation

- Create a tab to document data cleaning steps and updates.
- Organize the spreadsheet for better usability:
  - Freeze rows and columns.
  - Resize column widths and wrap text as needed.
  - Add filters.

### Filter listings

- Download the [NYC Airbnb dataset](nyc_airbnb_data) and create a copy for reference.
- Filter out listings that may not be relevant:
  - Exclude listings that have never been rented.
  - Include only rentals with a minimum night requirement of 7 days or fewer.
  - Remove listings with no reviews in the last 12 months.

## Part 2 - Which type of properties should be targeted?

### Neighborhood attractiveness for vacation rentals

- Clean the neighborhood column for consistency.
- Create a new column `neighborhood_clean` to standardize capitalization and remove trailing spaces.
- Build a pivot table to identify the top 10 neighborhoods based on the most reviews in the last 12 months.

### Popular property sizes for vacation rentals

- Clean the bedrooms column to handle empty cells (studio apartments).
- Create a new column `bedrooms_clean` to substitute empty cells with zeros.
- Use a pivot table to determine the most popular property sizes.
- Analyze if different neighborhoods prefer specific property sizes.

## Part 3 - Calculating occupancy

### Prepare calendar data for occupancy calculation

- Convert the `available` column to numeric values (`0` for false, `1` for true) to create a new column `occupied`.
- Add a new column `day_of_week` using the WEEKDAY() function to differentiate weekends and weekdays.

### Calculate average occupancy rates

- Build a pivot table to calculate the average occupancy rate for each listing using the `occupied` column.
- Analyze which days of the week have higher occupancy rates.

## Part 4 - Estimate revenue for an investment property

### Estimating annual revenue

- Filter properties based on criteria such as high review ratings and active rental history.
- Calculate the average price and occupancy rate for properties in one of the top neighborhoods and recommended property sizes.
- Estimate annual revenue using the average price and occupancy rate.

## Part 5 - (Optional) What attributes are important for a vacation rental?

- Investigate if superhosts charge higher prices.
- Analyze if instant booking affects occupancy rates.
- Explore the impact of amenities like building staff on review scores.

## Part 6 - Documentation and spreadsheet formatting

### Organize and format your spreadsheet

- Create an Executive Summary sheet summarizing recommendations.
- Include a Table of Contents for easy navigation.
- Document all data cleaning steps and assumptions made in the analysis.
- Use consistent formatting for clarity and readability:
  - Add borders, background colors, and font styles where necessary.
  - Hide unnecessary columns to focus on relevant data.

### Project Submission

Share your polished Google Sheets file with the client for review and feedback.

---

**Dataset Download Link:** [NYC Airbnb Dataset](nyc_airbnb_data)
