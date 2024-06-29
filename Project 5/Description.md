# Storytelling with Data: Project Files

- **Superstore.xls**

What is causing the high number of returned orders at the Superstore? In this project, we will be preparing an analysis for the CEO of the Superstore to help them understand what is causing customers to return their orders and how to reduce the volume of returned orders.

Remember to use the rubric as a guide as you develop your project, and before submitting, make sure that you have met all of the criteria and demonstrated your mastery of the material.

## Storytelling with Data Rubric

### 1. What is Causing Returns?

In this section, we will be building worksheets analyzing different views on return rates.

- **HINT**: Make sure the Returns table is LEFT JOIN’ed onto the Orders table. You should see both “Yes” and “null” values in the Returned column.
- Make the Returned field into a calculated field where the null values are 0 and the Yes values are 1. Note that the average of this field is the return rate, while the total returns are the count or sum of returns.

Now, let’s try to find some root causes for returned orders. Build at least one worksheet for each of the following:

- A scatterplot showing the correlation between total sales and total returns. Aggregate by product subcategory. Do sales always correlate positively with returns?
- A bar chart showing the return rate by product category.
- The return rate by customer. To find customers who are more prone to making returns, add a filter to remove customers with only 1 order.
- A map showing the return rate by some geographic measure (state, city, etc.) to see if there is a geographic concentration to returned orders.
- The return rate by some measure of time (month, week, etc.) to see if there is a seasonal effect to returned orders.
- Two different kinds of composite charts showing the return rate for a mix of multiple factors (date/geography/product category/etc.).

### 2. Building a Dashboard for Monitoring Returns

In this section,

- Create a low-fidelity mock-up of your dashboard.
  - Make at least 3 variations of pen-and-paper sketches.
  - Scan or take photos of them to submit.
- Choose your favorite option: This is the one you'll be making in Tableau.
- Create a template for the dashboard using empty containers to match your mock-ups.
- Take a screenshot… You'll submit this along with the rest of the project files.
- Add your worksheets to the dashboard template.
- Finalize the dashboards with relevant markers, images, and titles as needed. Submit your mock-up, template, and finalized dashboard.

### 3. Presenting Your Analysis and Dashboard

Construct your story arc for your presentation.

- Create a draft of your story using only captions for each Story Point.
  - A summary of your analysis of returns.
  - How should returns be measured? Is the return rate, the total cost of returns or the total number of returns a better measure? When is one better than the other?
  - What are the key root causes of returns?
  - An overview of each component of your Dashboard.
  - Explain what is contained in each chart and how the chart should be interpreted.
  - A demonstration of how the Dashboard should be used.
  - Demonstrate how to interpret the Dashboard and how to use filters to identify root causes.
  - Describe actions that can be taken after using the Dashboard to identify the root causes.
  - A conclusion with proposed next steps (e.g., implementation of Dashboard).
- Add content to your Story Points.
- Use the worksheets you already created and create new worksheets you might need to support your Story Arc.
- Construct Dashboards to create presentation style slides.
- Save a version of your completed Tableau Story.
- Deliver your presentation.
- Prepare a 3 to 5 minute presentation of your Tableau Story.
  - You can either use a screen recording software to record a 3 to 5 minute presentation of your Tableau Story or submit the presentation in PDF format.
  
