# Boston airbnb data analysis

![Image of Yaktocat](https://octodex.github.com/images/yaktocat.png)

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

In addition to a basic linear regression, I decided to use both Ridge and Lasso regression models. These models handle sparse data sets well by reducing the dimensions in the model either to a very low coefficient or as in the case of Lasso, to zero.  This is a good choice to use with this dataset that has hundreds of variables to evaluate.

## Evaluation and intrepretation of the model.

The ridge regression performed the best with respect to the model score and cross-validation.  Ridge models minimize the coefficient values of irrelevant features their impact on the trained model.

As someone who is interested in pricing a rental property on airbnb, it is important to understand key factors in the pricing.  If you already have a property, then there are some aspects you cannot change (such as location and property type). However, this model's outputs can be used to make recommendations on other factors you may be able to impact.

I went out to find out a few things about Boston airbnb rental:

     1. Which neighborhoods in Boston have the highest rental prices? 
     
     2. What types of properties are the most expensive to rent?

     3. What time of year has the highest rental prices?

     4. How can we maximize our rental revenue?  What are the major factors that influence the price of an airbnb rental in Boston?

For the first question, I have included the average price by neighborhood:

You can see that the XXX, YYY an dZZZ properties draw the highest rents.  I also wanted to see the number of rental properties in those neighborhoods. The highest priced neighborhoods also seem to have fewer properties available for rent on airbnb.

GRAPH HERE

The property types also vary in price, as you can see below, the XXX and YYYY  property types garner the highest prices.

This time series chart provides an easy to see trend where the prices in 2017 dropped from 2016 and spiked in April during the Boston Marathon.

GRAPH HERE.

Finally, the big question about how to maximize rental revenue.  I used the aforementioned model to determine what the most important coefficients are. In this case, it's important to look at the large positive coefficients and the largest negative coefficients as well.  
GRAPH TOP 3-5 coeff, pos and neg.

There are several factors that are strongly positively correlated to price, such as the location, the type of property and the cancellation policy (note, I would infer that the strict policy is the result of the premium price, NOT the cause of it!)

The model confirms data we saw above where Bay Village, Leather District and the Back Bay neighborhoods are among the most expensive.  In addition, the property types of "Other", boat and entire home/apartment are also premium properties. 

On the other hand, there are several variables that are negatively correlated with the price. These variables include the property type of camper/RV, dorm, and private room. The lower priced neighborhoods include Hyde Park, Roslindale and Dorchester.  

The graphs above support these findings while the model's coefficients provide us a way to determine the impact of these variables on the prices.


## Deployment

