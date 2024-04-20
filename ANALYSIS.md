# ANALYSIS and Technical Results

I used the models listed below for my analysis.

## 1. Linear Regression

To check the notebook for linear regression [linear_regression](linear_regression.ipynb).

`On training set`

```
ElasticNet(max_iter=100000)
value of R2
0.9956225580219896
The value of Mean Squared Error is:  162.1680920810809
The root mean squared error is  12.734523629923537
```
* The value of R2 is 0.995 which is very close to 1 and it shows that the fit is great. A high R2 value for linear regression suggests an
excellent fit and shows strong relationship between the close and the open price. 

* But the value of mean square error and root mean square seems to be high so I have added parameters to input varaibale "VWAP","Volume","Trades","Low","Last","Prev Close" to predict the target variable "Close" and found that mean square error and root mean square error values reduces drastically which indicates that target variable has dependency on other features too.

```
value of R2
0.9999355795018
mean squared error is  2.3865420344755255
The root mean squared error is  1.5448436925707163
```


`On Test Set`

```
LinearRegression()
0.9999503574232372
mean squared error is  1.8901133262619518
The root mean squared error is  1.3748139242319128

```


## 2. Decision Trees

To check the notebook for decision trees [Classification](classification.ipynb).

`On training set`

```
Accuracy = 0.5266015200868621
Precision = 0.27730916095779384
Sensitivity = 0.5266015200868621
F1 = 0.3633026134311922
```

* Since the metrics are 0.56 for the training set, it was suspected that the decision tree was overfitting. In the next step, the decision tree was applied to the test set to evaluate its performance on unseen data.

`On Test Set`

```
Accuracy = 0.5618892508143323
Precision = 0.5561292382291975
Sensitivity = 0.5618892508143323
F1 = 0.4775368206817104
```

* Here analysis of the decision tree on the test set yeilded metrics that are close to the metrics of train set and the suspicion of the decision tree overfitting the training set might be wrong. However, an analysis of the data with Random Forrest classifier has been done and it will help to clarify things up a little more. 

## 3. SVM

To check the notebook on SVM [Classification](classification.ipynb).

```
Accuracy = 0.5266015200868621
Precision = 0.27730916095779384
Sensitivity = 0.5266015200868621
F1 = 0.3633026134311922
```

* SVM metrics seem to be poor. It could be because the dataset is imbalanced, or the kernel choice was not the best


## 4. Random Forrest
To check the notebook on Random Forrest [Clustering](clustering.ipynb).

```
Accuracy (training): 0.9998275340194038
Accuracy (testing): 0.9989571423141078
R2 score : 1.00
Mean squared error: 36.36
Root Mean squared error: 6.03
```

* To address overfitting of the decision tree metrics Random Forrest with 1000 trees was employed and high metrics yielded suggest it might not be overfitting. 

* Random Forrest seems to do a better job. The R2 score seems to be a perfect 1.0 which could be a result of slight overfitting. Overall random forrest does better than decision tree alone.

## Challenges Faced 

1. I don't think I can call it a challenge, but when I was performing the decision tree analysis on my data set, the model seemed to have poor performance on both train and test set. When used a random forest which yeilded very good results. 

2. Using SVM was also challenging task for me. The choice of the kernel was the difficult part. I used the linear kernel. 


## Improvements and Future Prospects

1. It would be interesting to use the date feature for prediction in order to analyse how the currency does during different times of the year. 

2. I think a different size of split might be particulary useful in order to make better prediction.

3. A PCA model can be employed in the future in order to determine if the predictions can be based off a single variable.

4. It would also be interesting to predict by how much the close price would increase given an open price and time of the year. 