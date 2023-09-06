# TG-python-MLP-cancer-diagnosis
Run on the data set at https://www.kaggle.com/datasets/athirags/cancer-details
This may be run in Kaggle or Jupyter Labs.

## EDA with descriptives, scatter plots, mutual information, followed by neural net prediction classifier. 
### Several improvements made: 
1. The original MLP was too large, literally learning noise and failing on validation checks.
2. The validation set was too small to keep near or below the training loss (an indicator that it is not fitting).
3. The new MLP (Multi Layer Perceptron) NN design shows the training and validation loss in a better shape.
4. The stopping function works as intended.
5. The code now runs with seeded random number generation for consistency / deterministic behavior.
6. Smaller batches usually help with producing better generalization.
7. The accuracy improved
8. A Cohen's Kappa test for the agreement of results is also pretty good.
9. Future exercise: three way split: test, validation, and training with stratifiction of each, would help confirm that the Cohen's Kappa is good. However, the total training set is fairly small so for now I'm leaving this for more thought - might also explore synthetic data but would have to test the stability of results with synthetic data.

There were a total of 14 changes in diagnosis 
Accuracy against the full training set is 0.9753954305799648 
Total changed from positive to negative 4 
Total changed from negative to positive 10 
True positives 202 
True negatives 353 
Calculated Observed Agreement = 0.9753954305799648 
Calculated Chance Agreement = 0.535157106631126 
Cohen's Kappa= 0.947069064040718 

Summary of prior results: 
1. Data requires no cleaning, descriptive statistics are shown.
2. Histogram demonstrates most data is close to normal. It turns out the SE features are the most skewed, and also found to generally have the least mutual information in regression analysis.
3. The scatter plots show general clustering of the diagnosis.
4. Mutual Information comes back with strong agreement on the use of the highest scoring 18 or 19 features.
5. A neural network is used as a binary classifier

Thank you to Athira G for making this data set available. I hope this notebook helps. Also, thanks to the Tutorial authors here on Kaggle. I did use ChatGPT to generate an example for mutual information regression, and in the end it is about the same as the code for use with categorical feature mutual information analysis from the tutorials.
