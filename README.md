# Mean_Normalization
In machine learning we use large amounts of data to train our models. Some machine learning algorithms may require that the data is normalized in order to work correctly. The idea of normalization, also known as feature scaling, is to ensure that all the data is on a similar scale, i.e. that all the data takes on a similar range of values. For example, we might have a dataset that has values between 0 and 5,000. By normalizing the data we can make the range of values be between 0 and 1.

Mean normalization will not only scale the data but will also ensure your data has zero mean.

We start by importing NumPy and creating a rank 2 ndarray of random integers between 0 and 5,000 (inclusive) with 1000 rows and 20 columns. This array will simulate a dataset with a wide range of values. 
We then perform mean normalization using the following equation:

`<Normalized_Column = (Col_Value – Mean)/Standard_Deviation>`

In other words, mean normalization is performed by subtracting from each column of XX the average of its values, and then by dividing by the standard deviation of its values. 

# Data Separation
After the data has been mean normalized, it is customary in machine learnig to split our dataset into three sets:
* Training Set
* Cross Validation Set
* Test Set

The dataset is usually divided such that the Training Set contains 60% of the data, the Cross Validation Set contains 20% of the data, and the Test Set contains 20% of the data. 
Each data set will contain rows of X_norm chosen at random, making sure that we don't pick the same row twice. This will guarantee that all the rows of X_norm are chosen and randomly distributed among the three new sets.
