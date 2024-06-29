# Project

## DATASET

Business Analytics Project

## Coworking Time

Turning event logs into business metrics

Congratulations, you’ve been hired as a junior analyst at an e-commerce company! After searching for months, the company has finally found the right candidate to analyze their raw transaction logs, and they want you to get started immediately.

Open the Business Analytics Project Google spreadsheet at the top of this lesson and explore the data in the “raw_user_activity” tab. Each row represents an activity, or event, by a user on the company’s website. Each time a user views a product page, opens their shopping cart, or completes a purchase, the event is captured in the activity logs.

### Dataset Details:

- **user_id**: Unique customer IDs
- **event_type**: Type of activity by the user
- **category_code**: Category of the product being viewed or purchased
- **brand**: Company that makes the product
- **price**: Price of the product, in USD
- **event_date**: Date of the user activity, in YYYY-MM-DD format

## Part 1: Build a conversion funnel

The executive team is interested in understanding how well the website is converting product page views into purchases. Your first job is to create a conversion funnel to better understand how users interact with the website.

1. Using data from the “raw_user_activity” sheet, create the funnel in a pivot table as a new sheet called “conversion_funnel”.
2. Ensure you count unique users for each stage of the funnel (Hint: the funnel should have 3 stages).
3. Use formulas to create two new columns in your pivot table: total conversion rates and conversion rates to the next step (Hint: reference the Overview of Funnels lesson).

## Part 2: Prepare data for cohort analysis

The company wants you to build acquisition cohorts based on the month of a user’s first purchase, and they want you to track cohort metrics month by month.

### Filter purchases:

- Create a new blank sheet tab called “purchase_activity”.
- Using the filters in the “raw_user_activity” sheet, select only event types that are purchases.
- After applying the filter, copy the entire sheet and paste the data into your “purchase_activity” sheet.
- Double check that you only have data for purchase events in the new sheet (Hint: there should be 4,845 rows in the new sheet, including column headers).
- Don’t forget to reset the filter in the “raw_user_activity” sheet after you’re done copying the purchase data.

### Calculate first purchase dates:

- Using the “purchase_activity” sheet data, insert a pivot table as a new sheet called “first_purchase”.
- Configure the settings of the pivot table to calculate the minimum event_date for each user.
- Transfer the first purchase dates to a new column in the purchase activity data.

### Set up monthly data to build and track cohorts:

- Create three new columns in the “purchase_activity” sheet: event_month, first_purchase_month, and cohort_age.
- Use the TEXT() function to create event_month in column H and first_purchase_month in column I (Hint: use the YYYY-MM format for your months).
- Use the DATEDIF() function to create cohort_age in column J as the number of months between the first purchase and the event (Hint: cohort ages should range from 0 to 4 months).

## Part 3: Calculate retention rates

The last steps of the analysis are to aggregate the purchase data into cohorts and then calculate retention rates for each cohort month by month.

### Group data into cohorts:

- Using the data from the “purchase_activity” sheet, insert another pivot table as a new sheet called “cohort_analysis”.
- Configure your pivot table so that each represents one cohort, which are based on the month in which customers made their first purchase (Hint: there should be 6 cohorts).
- The pivot table should also have the count of unique users for each cohort_age in the columns of the pivot table.

### Calculate overall retention rates:

- Create a new blank sheet called “retention_rates”.
- Add row labels for each cohort in chronological order.
- Add column labels that represent the cohort ages from 1 to 4 months (you can’t calculate retention rates for a cohort’s first month, so you don’t need to include age 0).
- Write a formula that calculates the retention rate for each cohort at each cohort age in the table you created, based on the starting cohort sizes (Hint: use a fixed column reference in your formula).

## Part 4 - Organize and document your spreadsheet

You’ve completed the calculations for your analysis, but you want to make sure your first project looks polished and professional before submitting it to the executive team. Apply some best practices that you learned in the Advanced Spreadsheets course.

- Fill in the results synopsis and analysis descriptions in the “Executive Summary” sheet:
  - Results — Briefly summarize the results and conclusions from your analysis:
    - The “conversion_funnel” sheet
    - The “retention_rates” sheet
  - Analysis — Explain important properties about the data and any assumptions you made in your analysis:
    - Describe the raw data (e.g., timespan, event types, how it was collected, what parts of it you actually used, etc.).
    - Explain what data you used to calculate the conversion rates in your funnel (e.g., user counts, number of transactions, or something else?).
    - Explain the decisions you made in your cohort analysis of retention rates (e.g., how did you form cohorts, over what time were you tracking them, and how did you calculate retention rates?).

- Reorder the sheets tabs so that the “Table of Contents” and “Executive Summary” sheets come first, followed by the sheets with your analytical results, then the sheets used for calculations, and finally the raw data sheets last. Use a legend to help organize the sheets.

- Format your spreadsheets for readability (e.g., format numbers and dates, add borders to tables, utilize bold fonts for column headers, freeze rows, highlight cells with calculations).

- Use your best judgment to make a spreadsheet that you’d like to receive if you were an executive.

## Project submission

To submit your project to reviewers, send them a link to your Google Sheets file. Click the Share button in the top right of the window to give view-only access to anyone with the link. That way, reviewers can check your work without accidentally changing anything in your spreadsheet.
