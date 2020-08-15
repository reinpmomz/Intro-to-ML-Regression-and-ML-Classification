# Intro-to-ML-Regression-and-ML-Classification

## Linear Regression (OLS): Predicting Fuel efficiency of cars

Walk through steps in the process of formulating a Machine Learning regression model. In particular, the models formulated here are obtained by using the method of Ordinary Least Squares.

The aim is to develop some models to predict the fuel-efficiency of vehicles given other known characteristics of the vehicles.

The data was obtained from https://www.fueleconomy.gov/feg/download.shtml and contains information about model year 2020 vehicles sold in the United States.

What do the variables in the data represent?

- `make`

- `model`

- `mpg`, miles per gallon rating

- `transmission`, Automatic, CVT, or Manual

- `gears`, number of gears

- `drive`, drivetrain: 4WD, AWD, FWD, PT 4WD, RWD

- `disp`, engine displacement (in liters)

- `cyl`, number of cylinders

- `class`, vehicle category: Compact, Large, Mid St Wagon, Midsize, Minicompact, Minivan, Sm Pickup Truck, Sm St Wagon, Sm SUV, SPV, Std Pickup Truck, Std SUV, Subcompact, or Two Seater

- `sidi`, Spark Ignited Direct Ignition: Y or N

- `aspiration` Natural, Super Super+Turbo, Turbo

- `fuel`, primary fuel type Diesel, Mid, Premium, Regular "

- `atvType`, alternative technology: Diesel, FFV, Hybrid, None, or Plug-in Hybrid

- `startStop`, start-stop technology Y or N

### Simple Linear Regression

In simple linear regression, we are aiming to find a linear relationship between one outcome variable and a single predictor variable:

`y=α+βx`

There are many potential techniques for finding the model coefficients. We will be starting with Ordinary Least Squares (OLS).

We can use the lm function to fit an OLS model. lm requires two inputs:

a formula specifying the output variable and the predictors you intend to use

a dataframe containing the variables in the formula

### Multiple linear regression

In multiple linear regression, we are attempting to formulate a linear model using more than 1 predictor.

For a case of n variables, we are looking for a model of the form:

`y=α+β1x1+β2x2…+βnxn`

As in the case of simple linear regression, there is an intercept term. However there are now coefficients for each predictor in the model.

## Regression (Decision Trees)

Decision trees work by using the following general framework:

- splitting the training data into smaller and smaller groups based on cutoff values of chosen input variables

- Each split of the data creates what is called a node of the tree

- the process is stopped when some previously-stated stopping criterion/criteria, Some possible stopping conditions:

 * the three should be no more than 3 levels deep

 * No node containing < 5% of the data can be split further

- model values can then be predicted by taking a representative value (typically the mean) of the training subjects in the same node as the subject we are predicting for

There are many different techniques for choosing the variables to branch on. We will be using the CART method as implemented in the rpart package. The algorithm used by rpart adheres very closely to the method as described in Breiman et. al (1984).

## Classification

This case study is taken from Supervised Machine Learning Case Studies in R by Julia Silge.

### Exploring the Stack Overflow Survey

- Print the stackoverflow object.

- In the calls to count(), check out the distributions for remote status first, and then country.
