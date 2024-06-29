# Project Datasets

- **Superstore.xls**

Welcome to your Data Visualization project! To ensure fair and consistent evaluation, we’ve created this project rubric. The rubric outlines the criteria and standards we will use to grade your project. We recommend using it as a guide while developing your project to ensure you meet each criterion and demonstrate mastery of the material.

## Data Visualization Rubric

![Coworking Time Saving SuperStore](image)

### Part 1: Profits & losses

First, we'll identify the important centers of profit and loss for the superstore.

- Among the pairs of dimensions (e.g., subcategory + region, or shipping mode + product ID), identify the two biggest profit centers and two biggest loss-makers. Justify your conclusion with a visualization.
- Which products should the superstore stop selling? Justify your conclusion with a visualization.
- Which product subcategories should the store focus on and which should they stop selling? Choose 3 of each.

### Part 2: Advertising

The superstore wants to assess the profitability of advertising.

- Identify the 3 best combinations of states and months of the year to advertise in. Visualize the average profit for each month of the year for those 3 states and justify the advertising spend.
- Determine the optimal advertising spend based on the return on ad spend ratio. Allocate up to 1/5 of profits for advertising in this exercise.

### Part 3: Returned items

In this part, use the Returns table to analyze return rates.

- **HINT**: Ensure the Returns table is LEFT JOIN’ed onto the Orders table to see both “Yes” and “null” values in the Returned column.
- Create a calculated field where null values are 0 and Yes values are 1 to analyze return rates.
- Visualize:
  - Which products have the highest return rate?
  - Which customers have the highest return rate?
- Create a visualization of average profit against average return rate on a chosen dimension (state, shipping mode, product type, etc.) to support decisions on continuing or discontinuing business based on this dimension.

### Part 4: Submitting your project

You need to submit a ZIP archive of your project. It should include:

- README.md file with a link to the workbook on Tableau Public's server (publish your dashboard on Tableau Public and insert the link).
- All of your files (including additional files as needed — ensure they are no more than 9 megabytes in total).
