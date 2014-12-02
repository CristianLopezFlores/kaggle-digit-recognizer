# Digit Recognizer

Basic Kaggle competition for recognizing digits using the MNIST
("Modified National Institute of Standards and Technology") dataset.

[Competition details](http://www.kaggle.com/c/digit-recognizer)

## Requirements

* Julia >= 3.0
  * DataFrames package
  * DecisionTree package
* iJulia
* Datasets in `./data` or on the [competition page](http://www.kaggle.com/c/digit-recognizer/data)

## Running

Start up ipython notebook `ipython notebook --profile julia` and open
the `DigitRecognizer.ipynb` notebook

## Results

Using a random forest of 10 random features, 10 trees, and 0.5 portion of
samples per tree builds a model of:

```julia
Ensemble of Decision Trees
Trees:      20
Avg Leaves: 3426.75
Avg Depth:  24.4
```

Using a 5 fold cross validation the mean accuracy for prediction the correct
digit is `Mean Accuracy: 0.9388095238095238`

This is relatively good using a decision tree on digit recognition versus
a k nearest neighbors approach which might yield better accuracy.

At time of submission this accuracy ranked `#368` on the [leaderboard](http://www.kaggle.com/c/digit-recognizer/leaderboard).
