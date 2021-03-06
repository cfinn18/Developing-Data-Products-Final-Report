Developing Data Products Final Presentation
========================================================
author: Chapman Finn
date: 08/19/17
autosize: true

Course Project
========================================================

This Shiny app was created for the Developing Data Products course from Coursera's Data Science Specialization. 
The goals of this project are:
- To demonstrate the use of Shiny to build web applications
- Create a reproducible pitch for the application

The App: Diamond Appraisal
========================================================
This application utilizes the <code>diamonds</code> dataset from the <code>UsingR</code> package to predict the price of a diamond
described by a chosen set of parameters. 

All the user must do is input the appropriate values for each parameter and the app will output the estimated cost of such a diamond.


Prediction
========================================================
This code block shows the model and prediction I use to estimate price.
The relevant parameters chosen are:
- Carat
- Cut Quality
- Color
- Price

Price and Carat require transformations to make the primary relationship linear so regression can be performed.

```r
model <- lm(log_price ~ cube_carat + carat + cut + color + clarity, data = myData)
```

Data table view
========================================================

This tab panel allows to filter the rows present in the dataset according to three variables:

- Carat
- Cut
- Color

Only those rows matching the selection will be rendered


The app
========================================================
The source code can be located at: 
https://github.com/cfinn18/Developing-Data-Products-Final-Report

The app itself is hosted here: 
https://cfinn18.shinyapps.io/DDP-Shiny/
