# Customer Geography Analysis

## Problem Statement

We aim to gain insights into our customer base by analyzing their addresses and total spending. This investigation will help us:

* Identify potential underserved cities with low spending, indicating growth opportunities.
* Determine if our customer base is primarily concentrated in London or spread across other regions.

## Goals

The analysis will achieve the following:

* Calculate total customer spend per city.
* Compare London's spending to the rest of the UK.
* Identify potential data issues and cleaning methods.

## Data

The analysis utilizes a provided dataset containing:

* Customer address
* Total spending

## Methodology

1. **Data Exploration:**
    * Explore the customer address data to understand its format and identify missing values.

2. **City Extraction:**
    * Develop a method to extract the city name from the address field. This might involve:
        * Applying rules based on address length.
        * Using a predefined list of cities for comparison.
        * Extracting postcodes for cross-referencing with a national database (subject to permission).

3. **Data Cleaning:**
    * Address missing addresses (drop or categorize) and identify any unusual spending values.

4. **Customer Spend Analysis:**
    * Calculate the total customer spend for each city.
    * Compare the total spend in London to the rest of the UK, considering both all cities and excluding the "Other" category.

5. **Visualization:**
    * Create a bar chart to visualize the top 20 spending cities.

## Results

* A significant portion of addresses fall under the "Other" category, indicating limitations in the city extraction method.
* London exhibits the highest total customer spend compared to other large cities.
* Spending patterns don't necessarily correlate with population size (e.g., Leeds).

## Conclusion

Our customer base leans towards London, with a high concentration of spending in Manchester, Birmingham, and Glasgow. While these cities boast high populations, spending seems to vary, suggesting further investigation into customer demographics and marketing strategies. 

**Further Considerations:**

* Refining the city extraction method to capture more addresses.
* Exploring spending patterns by customer segments beyond city location.
* Analyzing customer acquisition channels for different regions.

This analysis paves the way for further exploration of customer geography and its impact on spending habits. By delving deeper into this data, we can make informed decisions about resource allocation and marketing strategies to reach a wider customer base across the UK.