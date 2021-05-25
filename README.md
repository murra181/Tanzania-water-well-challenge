# Tanzania Water Challenge -
This is the classification challange from drivendata.org

![Tanzania climate classification map] (https://github.com/murra181/Tanzania-water-well-challenge/blob/main/Media/Tanzania%20climate%20classification%20map.jpg)

## Business Case - 
Using data provided from drivendata.org for the "Pump it Up: Data Mining the Water Table" Challenge I will be building a model to predict if a well is functional, functional but in the need of a repair, or not functional. Accuracy is what is being judged so this is what my models will be trained for.

## EDA -
Looked through each column to see what had to many unique variables what was viable and what were mere copies or generalized forms of other columns. I reduced the columns from thirty nine independent variables to just twenty and got rid of 4,788 rows that were missing data. Categorical features were then dummied and readied for modeling

## Baseline models -
We will be looking at accuracy for four base models as they are what makes the most sense for a ternary classification and the data we have.

Decision Tree: 74.56%

Random Forest: 78.55%

Adaboost: 72.14%

Bagged Trees: 78.6%

Random forest and bagged trees are very similar so it makes sense that they are so close. I took the Random Forest model and Hyperparaeter Tuned it.

## Final Model -

GridSearchCV was used on the Random Forest Model an increased the accuracy by 1.16% to 79.61%
I then Bagged the model and increased it to 80.11% 

## Conclusion - 
The model was accurately able to predict whether a pump was was functional, functional but needs repaired or not functional at 80.11% 
This is what the competition was looking for but the biggest part that I think needs improving for this data to be useful is that 13.75% of wells predicted as functional were not.


## Future Work - 
Remove outlier and bin more of the continous data to see if improvements can be made across the board. 

Latitude and longitude were important features in the desicion tree and random forest but when you think about it have nothing to do with a well breaking down so I would like to remove these and gps height and focus more on basin and regions. 

Also want to focus on a bigger break down of the eda to then determine which variables are interacting with each other

Predict and submit to the challenge

