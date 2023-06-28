## CASE STUDY - FACE IDENTIFICATION

In this document, we walk through some helpful tips to get you started with building your own 
application for classifying faces in photo images using Principle Component Analysis (PCA)

#### 1:Standardize the data.
The PCA works on maximizing the variance.It projects the original data into directions which maximize the variance. So we should standardized the variables before applying PCA because it will give more importance to those variables having higher variances than to those variables with very low variances while identifying the right principle component. If you Standardize the data, all variables have the same standard deviation, thus all variables have the same weight and your PCA calculates relevant axis.
#### 2:Calculate the Covariance Matrix
Variance and Covariance are a measure of the spread of data around their mean. For PCA We need to study the relationships between the variables involved in a dataset, to be able to create new variables that can reduce the number of original values, without compromising on the information contained in them. The new variables are formed on the basis of correlations between the original variables.A covariance matrix expresses the relationship between the different variables in the dataset.Covariance is measured between 2 dimensions to see if there is a relationship between the 2 dimensions for example discount & Number of sales. The covariance with itself is the variance.
####  3:Compute Eigenvalues and EigenVectors of the covariance matrix.
The covariance matrix which we have calculated is then decomposed into eigenvalues and eigenvectors. Eigenvectors are those vectors when a linear transformation is performed on them, their direction does not change. They don’t change their direction they just scale the vector upwards or downwards. The value at which it scales is called the eigenvalue usually denoted by lambda.
#### 4:Selecting Number of components using Explained Variance
The desired goal is to reduce the dimensions of a d-dimensional dataset by projecting it onto a (k)-dimensional subspace in order to increase the computational efficiency while retaining most of the information. So the important question is what is the size of k that represents the data well?
We have got the eigenvalues and eigenvectors.Here we are going to find the number of components(k) which can explain maximum amount of variance.
#### 5:Projecting the data into lower dimensions.
The last step is to re-arrange the original data with the final low dimensional space (principal components) which represent the maximum and the most significant information of the data set. In order to replace the original data axis with the newly formed Principal Components, you simply multiply the transpose of the original data set by the transpose of the obtained feature vector.
