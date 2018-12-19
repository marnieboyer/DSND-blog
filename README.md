# Boston airbnb data analysis

1. Installations

2. Project Motivation

3. File Descriptions

4. How to Interact with your project

5. Licensing, Authors, Acknowledgements, etc.




## Business Understanding

1. Which neighborhoods in Boston have the highest rental prices?

2. What time of year has the highest rental prices?

3. How can we maximize our rental revenue? 

What are the major factors that influence the price of an airbnb rental in Boston?

## Data Understanding

The data used in this analysis includes listings data for over 3000 properties for rent in Boston on the website airbnb (listings.csv) and a file with daily pricing and availability of those properties.  The data is for one year (Sep 2016 to Sep 2017). In addition, there was a detailed file of reviews of those properties but it was not used in the analysis.

## Data Preparation

The data required several clean-up steps.  There were several columns with a majority of null data, so those columns (square feet, XXXX) were removed. Other columns (XXX, YYYY) with a few null values had values imputed from the average. This method seemed reasonable given the small amount of missing values.  If these columns had more missing data, there are more advanced ways to impute these metrics.

The data types also required a change so they can be used in calculations. The price, number of bedrooms, bathrooms, XXX, YYY had to be changed to numeric values.

The dataset also included categorical data, so those columns (neighborhood and amenities) were encoded. Amenities had first to be split  in order to separate each of the amenities into their own column. This increased the number of columns and made the dataframe quite sparse.

I explored the data to find out some high-level relationships and counts. First, I looked at the XXX and found YYY

Next, I explored the XXXX and saw NNNNN

## Modeling

The model was developed in order to understand what drives the price of airbnb rentals in Boston.  I attempted three different regression models.  I started with a basic linear model. First, I split the data into test/train datasets and normalized the data to ensure the variables are intrepreted correctly.

In addition to a basic linear regression, I decided to use both Ridge and Lasso regression models.

The ridge regression performed the best with respect to the model score.  Ridge models minimize the coefficient values of irrelevant features their impact on the trained model.



## Evaluation
## Deployment

