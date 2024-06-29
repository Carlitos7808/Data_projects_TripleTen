# Power BI: Project Dataset

- **shopify.xlsx**

## Shopify App Analysis

You have been hired to review the landscape of apps on the Shopify platform, using data scraped from publicly available Shopify websites. Your goal is to determine the key factors contributing to the success of Shopify apps.

### The Data

The shopify.xlsx dataset contains public data scraped from the Shopify App Store. It includes 4 tables:

- **apps**: Details of the apps on Shopify apps marketplace
- **apps_categories**: Join tables to connect apps with categories
- **categories**: Categories of the apps. Each app has multiple categories
- **reviews**: Each review (row) contains information on user opinion about the related app (rating and comment), and developer responses if present.

### Part 1: App Landscape

First, we’ll analyze key statistics on the types of apps available using the Apps table.

- Make a new sheet in your Power BI (.pibx) file called App Landscape for this question. Remember to take a screenshot for each question answered.
- Make a KPI Card (a visual with a single number) that counts the unique number of apps. Add it to your App Landscape sheet.
- Make a Line Chart showing the sum of review count on the Y-axis and the lastmod date on the X-axis. Hint: lastmod date should not be in “date hierarchy” format for your X-Axis.
- Make a Scatterplot with reviews_count on the X-axis and average rating on the Y-axis. Annotate your interpretation with a Text Box next to the scatterplot.

### Part 2: Reviews

Create a new sheet named Reviews in your .pibx file for this section. Remember to take a screenshot for each question answered.

- Create a new column in the Reviews table named helpful_reviews using a DAX expression: `rating * (1 + helpful_count)`. Make a Card with the average value of the new helpful_reviews column.
- Create a new column in the Reviews table named developer_answered using a DAX expression: `IF(NOT(ISBLANK(reviews[developer_reply])), 1, 0)`. Make a scatterplot comparing average rating on the Y-axis by the value of the developer_answered column on the X-axis.

### Part 3: App Reviews

Create a new sheet named App Reviews in your .pibx file for this section. Remember to take a screenshot for each question answered.

- In the data model, create a new relationship between the Reviews table and the Apps table using app_id (Reviews) to id (Apps) with a many-to-one relationship (Reviews to Apps).
- Create a bar chart with developer on the X-axis and sum of rating on the Y-axis using this new relationship.
- Create a new bar chart with developer on the X-axis and average of helpful_reviews on the Y-axis to avoid misleading information from sum of ratings.
- Identify the most responsive developers by creating a bar chart with developer from the Apps table and developer_answered column (from question 2.2). Add a filter to this visual to select rows where reviews_count is greater than 500.

### Part 4: Submitting your project

As .pibx files are too large to share, submit 8 screenshots:
- One screenshot for each sub-question on each page.
- Organize your .pibx project so that it contains one page for each section.
