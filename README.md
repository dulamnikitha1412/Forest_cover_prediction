
</p>
<h1 align="center"> Forest cover Prediction </h1>


  ![download](https://github.com/user-attachments/assets/dac69ce5-af2d-4e0e-aa46-7967d3dd4fd2)




<p> Build a system that can predict the type of forest cover using analysis data for a 30m x 30m
patch of land in the forest</p>


**Final version**: (https://github.com/dulamnikitha1412/Forest_cover_prediction/blob/main/nikitha.ipynb)

![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


We used the most typical classifiers that we covered in the course, with the exception of **Neural Networks** (week 7). These are:

- **k Nearest Neighbors** (week 2)
- **Naive Bayes** (week 3)
- **Decision Trees**, as well as **Random Forests**, **Extra Trees**, and **AdaBoost** (week 4)
- **Logistic Regression** (week 5)
- **Stochastic Gradient Descent** (week 6)
- **Support Vector Machines** (week 8)
- **Gaussian Mixture Models** (week 10) used for classification

  ![-----------------------------------------------------](https://raw.githubusercontent.com/andreasbm/readme/master/assets/lines/rainbow.png)


**AdaBoost combined with Extra Trees** yielded the best results, followed by **Extra Trees** alone, **Random Forests**, **Nearest Neighbors**, **SVMs**, **GMMs**, and **Decision Trees**. **Naive Bayes**, **Logistic Regression**, and **SGD** did not perform very well for this problem (and hence they are included in the Annexes at the end).

  ![image_28_7cf514b000](https://github.com/user-attachments/assets/5df023f5-d312-4298-8934-06cf6b293817)



The analysis of the existing features led us to engineer new ones, which we used to improve that best model (AdaBoost).

Finally I ensembled the results of the best 4 models (**kNN**, **AdaBoost**, **SVMs**, and **GMMs**), weighting them by their accuracy. (We excluded **Decision Trees**, **Random Forests**, and **Extra Trees** since they belong to the same family of methods than **AdaBoost**: they perform similarly, and also tend to make the same misclassification mistakes, so including the four would have "given them advantage" over the other three methods and overweighted those mistakes.)

Nonetheless, the predictions were not as accurate for the test set as they had been for the dev set we created from the training set, because the available data we had to train our models was quite different from the data we had to predict (the former was not a representative sample of the latter, or vice versa).

