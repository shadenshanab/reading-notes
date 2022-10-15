# class 06

## Data Analysis

----------------

[What is Jupyter Lab - Overview](https://jupyterlab.readthedocs.io/en/stable/getting_started/overview.html)

### JupyterLab is a next-generation web-based user interface for Project Jupyter

### JupyterLab enables you to work with documents and activities such as Jupyter notebooks, text editors, terminals, and custom components in a flexible, integrated, and extensible manner. For a demonstration of JupyterLab and its features

### You can arrange multiple documents and activities side by side in the work area using tabs and splitters. Documents and activities integrate with each other, enabling new workflows for interactive computing

- **Code Consoles** provide transient scratchpads for running code interactively, with full support for rich output.
- **Kernel-backed documents** enable code in any text file (Markdown, Python, R, LaTeX, etc.) to be run interactively in any Jupyter kernel.
- **Notebook** cell outputs can be mirrored into their own tab, side by side with the notebook, enabling simple dashboards with interactive controls backed by a kernel.
- Multiple views of documents with different editors or viewers enable live editing of documents reflected in other viewers.
JupyterLab understands many file formats (images, CSV, JSON, Markdown, PDF, Vega, Vega-Lite, etc.) and can also display rich kernel output in these formats.

----------------

### NumPy Tutorial

### NumPy is a commonly used Python data analysis package. By using NumPy, you can speed up your workflow, and interface with other packages in the Python ecosystem, like scikit-learn, that use NumPy under the hood. 

## Lists Of Lists for CSV Data

### Before using NumPy, we’ll first try to work with the data using Python and the csv package. We can read in the file using the csv.reader object, which will allow us to read in and split up all the content from the ssv file.

## Creating A NumPy Array

### We can create a NumPy array using the numpy.array function. If we pass in a list of lists, it will automatically create a NumPy array with the same number of rows and columns. Because we want all of the elements in the array to be float elements for easy computation, we’ll leave off the header row, which contains strings. One of the limitations of NumPy is that all the elements in an array have to be of the same type, so if we include the header row, all the elements in the array will be read in as strings. Because we want to be able to do computations like find the average quality of the wines, we need the elements to all be floats.

### import numpy as np.

### Creating an array from 0 to 9.

### arr = np. arange(10)

### print("An array from 0 to 9\n" + repr(arr) + "\n")​

## Numpy 2-Dimensional Arrays

### With NumPy, we work with multidimensional arrays. We’ll dive into all of the possible types of multidimensional arrays later on, but for now, we’ll focus on 2-dimensional arrays. A 2-dimensional array is also known as a matrix, and is something you should be familiar with. In fact, it’s just a different way of thinking about a list of lists. A matrix has rows and columns. By specifying a row number and a column number, we’re able to extract an element from a matrix.

## Using NumPy To Read In Files

### It’s possible to use NumPy to directly read csv or other files into arrays. We can do this using the numpy.genfromtxt function. We can use it to read in our initial data on red wines.

## Slicing NumPy Arrays

### If we instead want to select the first three items from the fourth column, we can do it using a colon (:). A colon indicates that we want to select all the elements from the starting index up to but not including the ending index. 

## Why use NumPy?

### NumPy arrays are faster and more compact than Python lists. An array consumes less memory and is convenient to use. NumPy uses much less memory to store data and it provides a mechanism of specifying the data types.

[read more](https://www.dataquest.io/blog/numpy-tutorial-python/)