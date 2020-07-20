# Intro-to-ML-Regression-and-ML-Classification

## Linear Regression (OLS): Predicting Fuel efficiency of cars

Walk through steps in the process of formulating a Machine Learning regression model. In particular, the models formulated here are obtained by using the method of Ordinary Least Squares.

The aim is to develop some models to predict the fuel-efficiency of vehicles given other known characteristics of the vehicles.

The data was obtained from https://www.fueleconomy.gov/feg/download.shtml and contains information about model year 2020 vehicles sold in the United States.

What do the variables in the data represent?

- make

- model

- mpg, miles per gallon rating

- transmission, Automatic, CVT, or Manual

- gears, number of gears

- drive, drivetrain: 4WD, AWD, FWD, PT 4WD, RWD

- disp, engine displacement (in liters)

- cyl, number of cylinders

- class, vehicle category: Compact, Large, Mid St Wagon, Midsize, Minicompact, Minivan, Sm Pickup Truck, Sm St Wagon, Sm SUV, SPV, Std Pickup Truck, Std SUV, Subcompact, or Two Seater

- sidi, Spark Ignited Direct Ignition: Y or N

- aspiration Natural, Super Super+Turbo, Turbo

- fuel, primary fuel type Diesel, Mid, Premium, Regular "

- atvType, alternative technology: Diesel, FFV, Hybrid, None, or Plug-in Hybrid

- startStop, start-stop technology Y or N

### Simple Linear Regression

In simple linear regression, we are aiming to find a linear relationship between one outcome variable and a single predictor variable:

y=α+βx

There are many potential techniques for finding the model coefficients. We will be starting with Ordinary Least Squares (OLS).

We can use the lm function to fit an OLS model. lm requires two inputs:

a formula specifying the output variable and the predictors you intend to use

a dataframe containing the variables in the formula




