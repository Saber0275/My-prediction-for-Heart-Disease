# My-prediction-for-Heart-Disease
Scaling and Normalizing

A new method in SkLearn: PowerTransformer & QuantileTransformer

“Numerical input variables may have a highly skewed or non-standard distribution.”


My background: I have been working on a dataset to predict the math score of students in 3rd Semester. Afterwards, I tried to use the so-called algorithms for scaling, MinMaxScaler and StandardScaler. However, I decided to explore deeply these algorithm to find out how they might change the data. This is simply because I heard from many Machine-learning Developers that they normally used Scaler algorithms to normalize! their data to be able to receive better results from their models. I had a vast majority of discussions with them that this method cannot normalize the data, it only scales the numerical variables and is sensitive to noise and outliers. Thereafter, I depicted some graphs that showed the distribution of numerical variables, like Histogram, and also I used Shapiro test and QQ Plot to convinced them that although scaling removes the outliers and is effective as a pre-processing step, it cannot normalize the data! Therefore, besides scaling, using some techniques that make our data to have more Gaussian-like distribution can be considered as a productive pre-processing step. My question was how could I normalize my data to have a more normally distribution in Python? Are there any straightforward techniques to do?
That is where “Power Transforms and Quantile Transforms” came to my attention. It is like parametric and non-parametric statistical tests. Parametric statistical tests are much more powerful than non-parametric tests.
According to an article by Brownlee applying a power transform feature-wise to make our data more Gaussian-like for the Machine learning algorithms that based on distances like Linear Regression and Gaussian Naive Bayes can be useful to have a more accurate model. Our data may have either Gaussian distribution or Gaussian-like distribution (with noise and outliers or completely different distribution).
As such, we may be able to achieve better performance on a wide range of machine learning algorithms (especially the ones that working with distances) by transforming input variables to have a Gaussian or more-Gaussian distribution by using 2 stream-line approaches called “PowerTransformer and QuantileTransformer”. Currently, PowerTransform supports the Box-Cox transform and the Yeo-Johnson transform.
In accordance with scikit-learn website:
1)	QuantileTransformer: provides non-linear transformations in which distances between marginal outliers and inliers are shrunk. This transformation tends to spread out the most frequent values. It also reduces the impact of outliers; this is therefore a robust preprocessing scheme and works much better than PowerTransformer.
2)	PowerTransformer: provides non-linear transformations in which data is mapped to a normal distribution to stabilize variance and minimize skewness.
-a) Box-Cox: can only be applied to strictly positive data.
-b) Yeo-Johnson: supports both positive or negative data
3)	Scalers: linear transformers in the way they estimate the parameters used to shift and scale each feature, and Scalers are sensitive to outliers as well. So, generally, Scalers remove noise and outliers from the data.
-a) StandardScaler removes the mean and scales the data to unit variance.
-b) MinMaxScaler rescales the data set such that all feature values are in the range [0, 1].
On balance, many machine learning algorithms (like KNN, Naïve-bayes) perform better when the distribution of variables is Gaussian, normally distributed. This means that this method does not work for any Machine learning algorithms, and also we have to check the accuracy of our model before and after normalizing by PowerTransformer/ QuantileTransforemer and scaling as well.
Note: For more elaborate information, please take a look at the HTML file.
