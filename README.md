# Knowledge based systems: NCAA Basketball Data Analysis

## Authors    

* Priyanka Sawant (psawant2@uncc.edu)     
* Keyurkumar Hansoti (khansoti@uncc.edu)    
* Urma Haldar  (uhaldar@uncc.edu)    

## Introduction
Every year college basketball fans participate in March Madness. They enter office pools or bet on the outcome of the 63 games that constitute the National Collegiate Athletic
Association’s (NCAA) basketball championship tournament. One web site indicated that billions of dollars are bet on the outcomes of games during this tournament. Moreover, Google
Scholar found over 18,000 references to the term “March Madness Betting”. Not all of these references are relevant to economics, but at least some include optimal betting strategies, e.g.
Metrick, 1995; Kaplan and Garstka, 2001; Clair and Letscher, (2007). So it is no surprise that there has been interest in methods for forecasting the outcomes of these games.

## Overview 
* The Project aims to predict basketball game outcomes using data analysis tools such Hadoop, BigQyery, PySpark.  
      
# Audience
* The interested audience are people who are into betting, game predictions as well as teams who can prepare themselves 
  against the predicted winning teams.

# Research Question:
* Who could possibly win the 2019 NCA Basketball Championship?
* What ML models could help improve such game predictions with more accuracy?

## Data 

* The Kaggle dataset "NCAA Basketball” will be used which is provided by the Kaggle.     
* The data set contains data about NCAA Basketball games, teams and players. The game data convers play-by-play-by
  and box scores back to 2009, as well as final scores back to 1996. Additional data contains wins and losses goes back
  to 1894-5 season in some teams cases.
* For this project, We are choosing mens basketball games from the 2014-14 season to the 2017-18 season.
* The data set contains 132 features like game_id, season, status, coverage etc.
* The size of the whole data set is around 4 GB.
*  #### Data Link: [NCAA Basketball Data Analysis](https://www.kaggle.com/ncaa/ncaa-basketball)
* For the pre-processing,we have removed some columns.
* We have uploaded the "Data Description_Domain Knowledge.docx" file containing the description of all the fields of the Data.

## Data Pre-processing

* Since, our data is pretty huge with over 132 attributes we have split our datasets into subsets.
* We have uploaded the data split in the subsets in the Kaggle data folder.
* The Data obtained is very clean and so for pre-processing we have done some name changes to the column names and have created distinct years for the season to fit our model requirements.

## Analysis

* First step we have done is to understand the domain, dataset and algorithms to be implemented.
* Based on the analysis we have created a dashboard based on various user groups.
* We have created a prediction model using Big Query.[2]
* Dashboards are hosted on Data studio of Google Cloud Platform.

## Approach to the solution

For our Data modelling, we have planned 3 approaches for prediction:

• Linear Regression-Linear regression is a basic and commonly used type of predictive analysis.  The overall idea of regression is to examine two things: (1) does a set of predictor variables do a good job in predicting an outcome (dependent) variable?  (2) Which variables in particular are significant predictors of the outcome variable, and in what way do they–indicated by the magnitude and sign of the beta estimates–impact the outcome variable?  These regression estimates are used to explain the relationship between one dependent variable and one or more independent variables.  The simplest form of the regression equation with one dependent and one independent variable is defined by the formula y = c + b*x, where y = estimated dependent variable score, c = constant, b = regression coefficient, and x = score on the independent variable.
For our NCAA data, we have used BigQuery ML model to do our Linear Regression, further details are in the document, UsingBigQueryInML.pdf., with queries and output.

• Logistic Regression- Logistic regression is a statistical method for analysing a dataset in which there are one or more independent variables that determine an outcome. The outcome is measured with a dichotomous variable (in which there are only two possible outcomes).
In logistic regression, the dependent variable is binary or dichotomous, i.e. it only contains data coded as 1 (TRUE, success, pregnant, etc.) or 0 (FALSE, failure, non-pregnant, etc.).
The goal of logistic regression is to find the best fitting (yet biologically reasonable) model to describe the relationship between the dichotomous characteristic of interest (dependent variable = response or outcome variable) and a set of independent (predictor or explanatory) variables. 
For our NCAA data we’ll be predicting possible matchup mixes for all teams, and winning teams as well using Python and model_selection with Jupyter Notebook. The results are better than linear regression.

• Gradient Boosting-A benefit of using gradient boosting is that after the boosted trees are constructed, it is relatively straightforward to retrieve importance scores for each attribute. Generally, importance provides a score that indicates how useful or valuable each feature was in the construction of the boosted decision trees within the model. The more an attribute is used to make key decisions with decision trees, the higher its relative importance.
For our NCAA data, we’ll be using XGBoost package of python, to predict matchups of all 2019 basketball games and try to predict the winners. The results are better than the previous.

Bracketology - Bracketology is the process of predicting the field of college basketball participants in the NCAA Basketball Tournament, named as such because it is commonly used to fill in tournament brackets for the postseason. It incorporates some method of predicting what the NCAA Selection Committee will use as its Ratings Percentage Index in order to determine at-large (non-conference winning) teams to complete the field of 64 teams, and, to seed the field by ranking all teams from first through sixty-eighth. Our document, Bracketology.pdf has our detailed workaround.

Neural Networks-Neural networks are a set of algorithms, modeled loosely after the human brain, that are designed to recognize patterns. They interpret sensory data through a kind of machine perception, labeling or clustering raw input. The patterns they recognize are numerical, contained in vectors, into which all real-world data, be it images, sound, text or time series, must be translated. 

## Dashboards
We have uploaded a Dashboards.docx in the github repository containing the screenshots of the Dashboards we have prepared in Data Studio.

## Work Division    
 The complete project has been accomplished together with collabrating and taking inputs from all the team members.
    
| Name | Task |     
| -- | -- |    
| Keyurkumar Hansoti | Research questions and definition of audience |   
| | Dashboards for User and Data Engineer |
| | Prediction using Bracketology 
| | Documentation of Team Members and Duties on Github |  
| Priyanka Sawant | Prediction using Linear and Logistic regression |
| | Evaluation of results |
| | Final Dashboard for User Group |
| | Presentation |
| Urma Haldar | Pre-processing of data |
| | Prediction using Gradient Boosting and Neural Networks |
| | Research citations | 
| | Documentation of Project Steps on Github |

## References, Citations and Abstract

# Abstract

The following papers have helped us understand the data, learn data analysis and data modelling. The authors have given a detail description to help understand the game and its attributes from user perspective which helps give a better insight to the project.[1] The authors have also explained the domain in detail highlighting the overall data and the goal.[2][3] The papers also helps understand how seeding affects the basketball games and contributes in the prediction of the winning and the loosing teams.[3] One can also learn how the prediction and outcomes are formulated as per the attributes which helps to better design the model.


# References

1. The National Collegiate Athletic Association (NCAA) basketball championship tournament (USA): statistics, prediction and analysis 
   https://ieeexplore.ieee.org/document/8148782
2. Predicting the Outcomes of NCAA Basketball Championship Game - H.O. Stekler and Andrew Klein
   https://pdfs.semanticscholar.org/6b96/36acfcf385d90ee85479140d37d1e98a733d.pdf
3. Determining the Success of NCAA Basketball Teams through Team Characteristics 
   https://digitalcommons.bryant.edu/cgi/viewcontent.cgi?article=1004&context=honors_mathematics

