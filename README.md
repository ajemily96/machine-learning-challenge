# Kepler Objects Analysis

## Intoduction

The Kepler space telescope is a deactivated space telescope designed to survey a portion of Earth's region of the Milky Way to discover Earth-size exoplanets. Acter being launched on March 7, 2009, the Kepler telescope opporated for 9 years, 7 months, 23 days, 8 hours, 10 minutes, and 33 seconds. All the time collecting data on planets orbiting stars to compare to earth. 

Though the Kepler telescope collected far more data, I decided to use only the Stellar Effective Temperature (koi_steff), 	Stellar Surface Gravity (koi_slogg), and the 	Stellar Radius (koi_srad) in my analysis to see if these 3 variables compined could reliably predict a planet's Exoplanet Archive Disposition. I utilized logorithmic regression, decision trees, random forest, Support Vector Classification, and Neural Networks as well as grid search functionality in attempt to optimize each model. 

## Results

- Logistic Regression
  - The grid search showed that the best version of the logistic regression with the 3 above stated variables was the first one tested (C=1) which came back with an score of ~0.5084 on the training data and ~0.4874 on the test data.

- Decision Tree
  - The grid search showed that the best version of the decision tree had max leaf nodes of 90 and minimum samples split of 2. This returned the score ~0.5525. An improvement over the logistic regression.

- Random Forests
  - The grid search showed that the best version of the random forest had the below parameters. This resulted in a score of ~0.5710, an improvement again!
    - {'criterion': 'entropy', 'max_depth': None, 'max_features': 1, 'min_samples_leaf': 10, 'min_samples_split': 3}

- Support Vector Classification
  - The grid search showed that the best version of the random forest had the below parameters. This resulted in a score of ~0.5056. Not an improvement over the Random Forest model.

- Neural Network
  - The Neural Network model returned an accuracy of ~0.4880 for the below specifications. Which is the lowest accuracy of any of the models.

## Conclusion
The Random Forest model most reliably predicts a planet's Exoplanet Archive Disposition using only the Stellar Effective Temperature, 	Stellar Surface Gravity, and the 	Stellar Radius data. Of course, utilizing more of the data could potentially create an even better model. Repeating this preocess with additional variables to determine if better models are available is advised. 
