# class 10

## Linear Regression

----------------------

### Linear regression is one of the fundamental statistical and machine learning techniques. Whether you want to do statistics, machine learning, or scientific computing, there’s a good chance that you’ll need it. It’s best to build a solid foundation first and then proceed toward more complex methods

### Scikit-learn is a powerful Python module for machine learning. It contains function for regression, classification, clustering, model selection and dimensionality reduction. Today, I will explore the sklearn.linear_model module which contains “methods intended for regression in which the target value is expected to be a linear combination of the input variables”.

### The first step is to import the required Python libraries into Ipython Notebook.

### This data set is available in sklearn Python module, so I will access it using scikitlearn. I am going to import Boston data set into Ipython notebook and store it in a variable called boston.

### The object boston is a dictionary, so you can explore the keys of this dictionary.

### I will see the description of this data set to know more about it. In this data set I have 506 instances(rows) and 13 attributes or parameters(columns). The goal of this exercise is to predict the housing prices in boston region using the features given.

### I am going to convert boston.data into a pandas data frame.

### As you can see the column names are just numbers, so I am going to replace those numbers with the feature names.

### I am going to add these target prices to the bos data frame.

