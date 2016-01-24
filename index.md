---
title       : Data Product Presentation 
subtitle    : Iris Species Prediction
author      : Kevin 
job         : Use Shiny to enable interactive web pages
framework   : io2012        # {io2012, html5slides, shower, dzslides, ...}
highlighter : highlight.js  # {highlight.js, prettify, highlight}
hitheme     : tomorrow      # 
widgets     : []            # {mathjax, quiz, bootstrap}
mode        : selfcontained # {standalone, draft}
knit        : slidify::knit2slides
---

## Project Overview

1. Use Shiny to realise interactive online data product
1. This Shiny application is Iris Species Prediction based on user inputs
1. Inputs: user can specify four features of Iris: Sepal.Length, Sepal.Width, Petal.Length, Petal.Width via web page input boxes (via ui.R)
1. Outputs: the predicted Iris Species (setosa, versicolor, virginica) is shown (via ui.R), which is reactive to whatever the plant feature value inputs
1. The machine learning random forest algorithm is used to process ui inputs at background to produce prediction results (via server.R)
1. The iris R dataset package is employed for this data product for simplicity
1. This pitch is done in Slidify

--- .class #id 

## Iris Data Summary
1. Following is the statistical summary of iris dataset using R
1. User inputs are bounded by the minimum and maximum values of each feature, and the default values are set to the median of each feature

```r
knitr::kable(summary(iris))
```



|   | Sepal.Length | Sepal.Width  | Petal.Length | Petal.Width  |      Species |
|:--|:-------------|:-------------|:-------------|:-------------|:-------------|
|   |Min.   :4.300 |Min.   :2.000 |Min.   :1.000 |Min.   :0.100 |setosa    :50 |
|   |1st Qu.:5.100 |1st Qu.:2.800 |1st Qu.:1.600 |1st Qu.:0.300 |versicolor:50 |
|   |Median :5.800 |Median :3.000 |Median :4.350 |Median :1.300 |virginica :50 |
|   |Mean   :5.843 |Mean   :3.057 |Mean   :3.758 |Mean   :1.199 |NA            |
|   |3rd Qu.:6.400 |3rd Qu.:3.300 |3rd Qu.:5.100 |3rd Qu.:1.800 |NA            |
|   |Max.   :7.900 |Max.   :4.400 |Max.   :6.900 |Max.   :2.500 |NA            |

---

## Iris Data Visualization     
1. Correlations between iris features Sepal.Length, Sepal.Width, Petal.Length, Petal.Width and iris species setosa, versicolor, virginica are shown below
1. It can be seen all these features are relevant and can be used as predictors for ML algorithm

![plot of chunk unnamed-chunk-2](assets/fig/unnamed-chunk-2-1.png)

---

## Conclusions
1. Shiny is a powerful tool to quickly enable interactive data products online
1. Users of Shiny need little or none knowledge of html and css to make web pages
1. Two key parts of Shiny: GUI is implemented by ui.R whereas service logics are done by server.R at background. Most efforts focus on server.R 
1. People can take advantage of Shiny to present and publish their data products to a mass population, for knowledge sharing and reproducible research
