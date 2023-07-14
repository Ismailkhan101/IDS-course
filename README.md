# IDS-course
What is data science?
Data science combines math and statistics, specialized programming, advanced analytics, artificial intelligence (AI), and machine learning with specific subject matter expertise to uncover actionable insights hidden in an organization’s data. These insights can be used to guide decision making and strategic planning.
Data science is a field of study that focuses on techniques and algorithms to extract knowledge from data. The area combines data mining and machine learning with data-specific domains. This section focuses on defining "data" before going to any complicated topic.
Python Basic Syntax 
## Python Basic Syntax
This is a basic Python program that uses the print() function to output the message "Hello, world!" to the console. It's often used as a simple starting point when learning a new programming language.
#
 print("Muhammad Ismail!")
## Variables and data types
This code demonstrates how to define variables in Python and assign them different data types. The name variable is a string, the age variable is an integer, the is_male variable is a boolean, and the height variable is a float.
#
 A=5 
B=3
 print(A+B) = 8
 Functions
This code defines a function square that takes a number as input, multiplies it by itself, and returns the result. The function is then called with an argument of 5 and the returned value is stored in the result variable. Finally, the value of result is printed to the console using the print() function.
### def square(x=5): return x*x
it print 25 which is square of five
##
In Python, you can define a function with an optional third parameter by providing a default value for the third parameter in the function definition. 
### Here's an example:

def add_num(x=2,y=3, z=None):
    if(z==None):
        return x+y
    else:
        return x+y+z
 #### p =add_num(4,5) =9	
 ## Update to take optional flag parameteer
 def add_num(x=2,y=3, z=None , flag=False):
    if(flag):
        print("flage is true")
    if(z==None):
        return x+y
    else:
        return x+y+z
	
 p =add_num(4,5, flag=True)
 ## There are several data types
 In Python programming, there are several data types that can be used to store different kinds of values. The most common data types include:
 #### Numeric types:
x = 42        # int
y = 3.14      # float
z = 1 + 2j    # complex

#### Boolean type:
is_true = True
is_false = False

#### List type
my_list = [1, 2, 3, 'four', 5.0]

#### Tuple type
my_tuple = (1, 2, 3, 'four', 5.0)

#### Dictionary type
my_dict = {'name': 'John', 'age': 30, 'city': 'New York'}

#### Set type
my_set = {1, 2, 3, 4, 5}
Python also provides a variety of built-in functions and methods for working with these data types, such as len(), append(), remove(), and many more.






bool (True or False)
Sequence types:

list (mutable ordered sequence of elements)
tuple (immutable ordered sequence of elements)
range (immutable sequence of numbers)
str (immutable sequence of characters)
bytes (immutable sequence of bytes)
bytearray (mutable sequence of bytes)
Mapping types:

dict (mutable key-value mapping)
Set types:

set (mutable unordered collection of unique elements)
frozenset (immutable unordered collection of unique elements)
## conditional statements
In Python, conditional statements allow you to execute different blocks of code depending on whether a certain condition is true or false. The most common conditional statements in Python are if, elif, and else.
####
a=8

if(a %2 ==0):
    print("this even number")
else:
        print("this Odd number")
#### for loop
In Python, the for loop is used to iterate over a sequence (such as a list, tuple, or string) or other iterable object (such as a dictionary or set) and execute a block of code for each item in the sequence. The basic syntax of a for loop in Python is as follows:
#####
numbers = [1, 2, 3, 4, 5]

for num in numbers:
    print(num)
## combine two lists
To combine two lists in Python, you can use the + operator or the extend() method. Here are examples of each method:

Method 1: Using the + operator
####
A=[1,2]
B=[3,4]
A+B = [1, 2, 3, 4]

## CSV files
In Python, you can read and write CSV files using the csv module. The csv module provides functionality for working with CSV files in a variety of formats, including comma-separated values (CSV), tab-separated values (TSV), and other delimiter-separated values.

To read a CSV file in Python, you can use the csv.reader() function. This function takes a file object as input and returns a reader object, which can be used to iterate over the rows in the CSV file. Here's an example:
####
import csv

with open('example.csv', 'r') as file:
    reader = csv.reader(file)
    for row in reader:
        print(row)
	
# NumPay

Numpy is the fundamental package for numeric computing with Python. It provides powerful ways to create, store, and/or manipulate data, which makes it able to seamlessly and speedily integrate with a wide variety of databases. This is also the foundation that Pandas is built on, which is a high-performance data-centric package that we will learn later in the course.

In this lecture, we will talk about creating array with certain data types, manipulating array, selecting elements from arrays, and loading dataset into array. Such functions are useful for manipulating data and understanding the functionalities of other common Python data packages.
## Import
when we want to utilize a library in our Python code, we use the "import" keyword. In the case of the widely used numerical computing library "NumPy," it is conventionally abbreviated as "np" in Python code. Therefore, we can refer to NumPy as "np" after importing it.
###
import numpy as np
##
import math
##
# Array Creation
NumPy is a powerful numerical computing library for Python that provides support for arrays, matrices, and mathematical operations on them. The np.array() function is a NumPy function that creates a new array object from a given list or array-like object. In this case, it creates a NumPy array with the values [1, 2, 3]. The resulting array is assigned to the variable a for further use in the code.
 ####
 a = np.array([1, 2, 3])
 ####
 print(a)
####
[1 2 3]
####
In NumPy, arrays can have one or more dimensions, which are also known as axes. The ndim attribute is a property of NumPy arrays that returns the number of dimensions of the array.
#####
print(a.ndim)
####
1
#####
a = np.array([[1,2,3],[1,2,3]])
####
print(a)
####
We can print the number of dimensions of a list using the ndim attribute
####
print(a.ndim)
####
The resulting array b is a two-dimensional array with shape (2, 3), meaning it has 2 rows and 3 columns, and contains the values from the list of lists provided. This can be visualized as a matrix with 2 rows and 3 columns, where the first row contains the values [1, 2, 3] and the second row contains the values [4, 5, 6].
####
b = np.array([[1,2,3],[4,5,6]])
####
 We can print out the length of each dimension by calling the shape attribute, which returns a tuple
####
b.shape
####
(2, 3)
####
We can also check the type of items in the array
####
a.dtype
####
Besides integers, floats are also accepted in numpy arrays
####
c = np.array([2.2, 5, 1.1])
####
c.dtype.name
####
'float64'
####
#### Note that numpy automatically converts integers, like 5, up to floats, since there is no loss of prescision.
#### Numpy will try and give you the best data type format possible to keep your data types homogeneous, which
#### means all the same, in the array
#### Sometimes we know the shape of an array that we want to create, but not what we want to be in it. numpy
#### offers several functions to create arrays with initial placeholders, such as zero's or one's.
#### Lets create two arrays, both the same shape but with different filler values
d = np.zeros((3,4,4))
####
#### Let's break down the code:

np.zeros(): This is a NumPy function that creates a new array object with a given shape and initializes all the elements to 0.

(3, 4, 4): This is a tuple specifying the shape of the array to be created. The tuple contains three integer values: 3, 4, and 4, representing the number of elements in each dimension of the array.

d = np.zeros(...): This assigns the created array to the variable d for further use in the code.

The resulting array d is a three-dimensional array with shape (3, 4, 4), meaning it has 3 slices, each with 4 rows and 4 columns, and all elements are initialized to 0. This can be visualized as a cube with 3 slices, each slice containing 4 rows and 4 columns, and all elements initialized to 0.

Note that the np.zeros() function can be used to create arrays of any dimension and shape, and the elements are initialized to 0 by default.
####
print(d)
####
####
[[[0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]]

 [[0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]]

 [[0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]
  [0. 0. 0. 0.]]]
#### 
print(d.ndim)
####
3
#####
e = np.ones((2,3))
####
print(e)
####
[[[0. 0. 0.]
  [0. 0. 0.]]

 [[0. 0. 0.]
  [0. 0. 0.]]]
[[1. 1. 1.]
 [1. 1. 1.]]
 #####
  We can also generate an array with random numbers
  ####
np.random.rand(2)
####
#### You'll see zeros, ones, and rand used quite often to create example arrays, especially in stack overflow
#### posts and other forums.
#### We can also create a sequence of numbers in an array with the arrange() function. The fist argument is the
#### starting bound and the second argument is the ending bound, and the third argument is the difference between
#### each consecutive numbers
####
import numpy as np
####
#### Let's create an array of every even number from ten (inclusive) to fifty (exclusive)
####
f = np.arange(1,15,.6)
####
f.ndim
####
#### if we want to generate a sequence of floats, we can use the linspace() function. In this function the third
#### argument isn't the difference between two numbers, but the total number of items you want to generate
#### 15 numbers from 0 (inclusive) to 2 (inclusive)
#####
np.linspace( 0, 2, 15 ) 
#####
#### We can do many things on arrays, such as mathematical manipulation (addition, subtraction, square,
#### exponents) as well as use boolean arrays, which are binary values. We can also do matrix manipulation such
#### as product, transpose, inverse, and so forth.
#### Arithmetic operators on array apply elementwise.
####
 Let's create a couple of arrays
 ####
a = np.array([10,20,30,40])
####
b = np.array([1, 2, 3,4])
####

 Now let's look at a minus b
 #####
c = a-b
#####
print(c)
#####

 And let's look at a times b
 ####
d = a*b
#####
print(d)
#####
[ 9 18 27 36]
######
[ 10  40  90 160]
#####
#### With arithmetic manipulation, we can convert current data to the way we want it to be. Here's a real-world
#### problem I face - I moved down to the United States about 6 years ago from Canada. In Canada we use celcius
#### for temperatures, and my wife still hasn't converted to the US system which uses farenheit. With numpy I 
#### could easily convert a number of farenheit values, say the weather forecase, to ceclius

#### Let's create an array of typical Ann Arbor winter farenheit values
#### farenheit = np.array([0,-10,-5,-15,0])

##### And the formula for conversion is ((°F − 32) × 5/9 = °C)
###### celcius = (farenheit - 31) * (5/9)
####

##### Great, so now she knows it's a little chilly outside but not so bad.
##### Another useful and important manipulation is the boolean array. We can apply an operator on an array, and a
##### boolean array will be returned for any element in the original, with True being emitted if it meets the condition and False oetherwise.
##### For instance, if we want to get a boolean array to check celcius degrees that are greater than -20 degrees
#### celcius > -20

#### Here's another example, we could use the modulus operator to check numbers in an array to see if they are even. Recall that modulus does division but throws away #### everything but the remainder (decimal) portion)
#### celcius%2 == 0
####
#### Besides elementwise manipulation, it is important to know that numpy supports matrix manipulation. Let's
#### look at matrix product. if we want to do elementwise product, we use the "*" sign
####
A = np.array([[1,1],[0,1]])
#####
B = np.array([[2,0],[3,4]])
#####
print(A*B)
####
[[2 0]
 [0 4]]
### # if we want to do matrix product, we use the "@" sign or use the dot function
print(A@B)
np.dot(A,B)

[[5 4]
 [3 4]]
array([[5, 4],
       [3, 4]])

#### You don't have to worry about complex matrix operations for this course, but it's important to know that
#### numpy is the underpinning of scientific computing libraries in python, and that it is capable of doing both
#### element-wise operations (the asterix) as well as matrix-level operations (the @ sign). There's more on this
#### in a subsequent course.
#### A few more linear algebra concepts are worth layering in here. You might recall that the product of two
#### matrices is only plausible when the inner dimensions of the two matrices are the same. The dimensions refer
#### to the number of elements both horizontally and vertically in the rendered matricies you've seen here. We
#### can use numpy to quickly see the shape of a matrix:

A.shape
#### When manipulating arrays of different types, the type of the resulting array will correspond to 
#### the more general of the two types. This is called upcasting.

#### Let's create an array of integers
array1 = np.array([[1, 2, 3], [4, 5, 6]])
####
print(array1.dtype)

#### Now let's create an array of floats
array2 = np.array([[7.1, 8.2, 9.1], [10.4, 11.2, 12.3]])
####
print(array2.dtype)
#### Integers (int) are whole numbers only, and Floating point numbers (float) can have a whole number portion
#### and a decimal portion. The 64 in this example refers to the number of bits that the operating system is
#### reserving to represent the number, which determines the size (or precision) of the numbers that can be
#### represented.
#### Let's do an addition for the two arrays
#### array3=array1+array2
#### print(array3)
#### print(array3.dtype)
#### Notice how the items in the resulting array have been upcast into floating point numbers
#### Numpy arrays have many interesting aggregation functions on them, such as  sum(), max(), min(), and mean()
print(array3.sum())
####
print(array3.max())
####
print(array3.min())
####
print(array3.mean())
####
#### For two dimensional arrays, we can do the same thing for each row or column
#### let's create an array with 17 elements, ranging from 1 to 15, 
#### with a dimension of 4X4
b = np.arange(1,17,1).reshape(4,4)
####
print(b)
####
[[ 1  2  3  4]
 [ 5  6  7  8]
 [ 9 10 11 12]
 [13 14 15 16]]
 ####
 #### Now, we often think about two dimensional arrays being made up of rows and columns, but you can also think
##### of these arrays as just a giant ordered list of numbers, and the *shape* of the array, the number of rows
##### and columns, is just an abstraction that we have for a particular purpose. Actually, this is exactly how
##### basic images are stored in computer environments.

##### Let's take a look at an example and see how numpy comes into play.
##### For this demonstration I'll use the python imaging library (PIL) and a function to display images in the
##### Jupyter notebook

from PIL import Image
####
from IPython.display import display

#### And let's just look at the image I'm talking about
im1 = Image.open('../chris.tiff')
#### display(im)
#### Now, we can conver this PIL image to a numpy array
array=np.array(im1)
####
print(array.shape)
####
array.ndim
####
(200, 200)
####
2
#### Here we see that we have a 200x200 array and that the values are all uint8. The uint means that they are
#### unsigned integers (so no negative numbers) and the 8 means 8 bits per byte. This means that each value can
#### be up to 2*2*2*2*2*2*2*2=256 in size (well, actually 255, because we start at zero). For black and white
#### images black is stored as 0 and white is stored as 255. So if we just wanted to invert this image we could
#### use the numpy array to do so

#### Let's create an array the same shape
mask=np.full(array.shape,255)
####
display(Image.fromarray(mask))
#### Now let's subtract that from the modified array
modified_array=array-mask

#### And lets convert all of the negative values to positive values
modified_array=modified_array*-1

#### And as a last step, let's tell numpy to set the value of the datatype correctly
####
modified_array=modified_array.astype(np.uint8)
####
modified_array.shape

#### And lastly, lets display this new array. We do this by using the fromarray() function in the python
#### imaging library to convert the numpy array into an object jupyter can render
display(Image.fromarray(modified_array))
#### Cool. Ok, remember how I started this by talking about how we could just think of this as a giant array
#### of bytes, and that the shape was an abstraction? Well, we could just decide to reshape the array and still
#### try and render it. PIL is interpreting the individual rows as lines, so we can change the number of lines
#### and columns if we want to. What do you think that would look like?
reshaped=np.reshape(modified_array,(100,400))
####
print(reshaped.shape)
####
display(Image.fromarray(reshaped))
# Indexing, Slicing and Iterating
Indexing, slicing and iterating are extremely important for data manipulation and analysis because these techinques allow us to select data based on conditions, and copy or update data.
#### First we are going to look at integer indexing. A one-dimensional array, works in similar ways as a list -
#### To get an element in a one-dimensional array, we simply use the offset index.
a = np.array([1,3,5,7])
####
a[2]
#### For multidimensional array, we need to use integer array indexing, let's create a new multidimensional array
a = np.array([[1,2], [3, 4], [5, 6]])
#### if we want to select one certain element, we can do so by entering the index, which is comprised of two
#### integers the first being the row, and the second the column
a[1,1] #### remember in python we start at 0!
####
4
#### if we want to get multiple elements 
#### for example, 1, 4, and 6 and put them into a one-dimensional array
#### we can enter the indices directly into an array function
np.array([a[0, 0], a[1, 1], a[2, 1]])
####
array([1, 4, 6])
# Boolean Indexing
#### Boolean indexing allows us to select arbitrary elements based on conditions. For example, in the matrix we
#### just talked about we want to find elements that are greater than 5 so we set up a conditon a >5 
print(a >5)
#### This returns a boolean array showing that if the value at the corresponding index is greater than 5
[[False False]
 [False False]
 [False  True]]
 ####
 #### We can then place this array of booleans like a mask over the original array to return a one-dimensional 
 ####array relating to the true values.
print(a[a>5])
####
[6]
# Slicing
#### Slicing is a way to create a sub-array based on the original array. For one-dimensional arrays, slicing 
#### works in similar ways to a list. To slice, we use the : sign. For instance, if we put :3 in the indexing
#### brackets, we get elements from index 0 to index 3 (excluding index 3)
a = np.array([0,1,2,3,4,5])
print(a[:3])
[0 1 2]
#### By putting 2:4 in the bracket, we get elements from index 2 to index 4 (excluding index 4)
print(a[2:4])
####
[2 3]
#### For multi-dimensional arrays, it works similarly, lets see an example
a = np.array([[1,2,3,4], [5,6,7,8], [9,10,11,12]])

#### First, if we put one argument in the array, for example a[:2] then we would get all the elements from the 
#### first (0th) and second row (1th)
a[:2]
#### If we add another argument to the array, for example a[:2, 1:3], we get the first two rows but then the
#### second and third column values only
a[:2, 1:3]
#### So, in multidimensional arrays, the first argument is for selecting rows, and the second argument is for 
#### selecting columns
#### It is important to realize that a slice of an array is a view into the same data. This is called passing by
#### reference. So modifying the sub array will consequently modify the original array

#### Here I'll change the element at position [0, 0], which is 2, to 50, then we can see that the value in the
#### original array is changed to 50 as well

sub_array = a[:2, 1:3]
####
print("sub array index [0,0] value before change:", sub_array[0,0])
####
sub_array[0,0] = 50
####
print("sub array index [0,0] value after change:", sub_array[0,0])
####
print("original array index [0,1] value after change:", a[0,1])

#### Trying Numpy with Datasets
#### Now that we have learned the essentials of Numpy let's use it on a couple of datasets
#### Here we have a very popular dataset on wine quality, and we are going to only look at red wines. The data
#### fields include: fixed acidity, volatile aciditycitric acid, residual sugar, chlorides, free sulfur dioxide,
#### total sulfur dioxidedensity, pH, sulphates, alcohol, quality
#### To load a dataset in Numpy, we can use the genfromtxt() function. We can specify data file name, delimiter
#### (which is optional but often used), and number of rows to skip if we have a header row, hence it is 1 here

#### The genfromtxt() function has a parameter called dtype for specifying data types of each column this
#### parameter is optional. Without specifying the types, all types will be casted the same to the more
#### general/precise type
wines = np.genfromtxt("datasets/winequality-red.csv", delimiter=";", skip_header=True)

graduate_admission.shape
#### We can retrieve a column from the array using the column's name for example, let's get the CGPA column and
#### only the first five values.
graduate_admission['CGPA'][0:5]
array([9.65, 8.87, 8.  , 8.67, 8.21])
#### Since the GPA in the dataset range from 1 to 10, and in the US it's more common to use a scale of up to 4,
#### a common task might be to convert the GPA by dividing by 10 and then multiplying by 4
graduate_admission['CGPA'] = graduate_admission['CGPA'] /10 *4
graduate_admission['CGPA'][0:20] #let's get 20 values
#### Recall boolean masking. We can use this to find out how many students have had research experience by
#### creating a boolean mask and passing it to the array indexing operator
len(graduate_admission[graduate_admission['Research'] == 1])
#### Since we have the data field chance of admission, which ranges from 0 to 1, we can try to see if students
#### with high chance of admission (>0.8) on average have higher GRE score than those with lower chance of
#### admission (<0.4)

#### So first we use boolean masking to pull out only those students we are interested in based on their chance
#### of admission, then we pull out only their GPA scores, then we print the mean values.
print(graduate_admission[graduate_admission['Chance_of_Admit'] > 0.8]['GRE_Score'].mean())
print(graduate_admission[graduate_admission['Chance_of_Admit'] < 0.4]['GRE_Score'].mean())
#### Take a moment to reflect here, do you understand what is happening in these calls?

#### When we do the boolean masking we are left with an array with tuples in it still, and numpy holds underneath
#### this a list of the columns we specified and their name and indexes
graduate_admission[graduate_admission['Chance_of_Admit'] > 0.8]
#### Let's also do this with GPA
print(graduate_admission[graduate_admission['Chance_of_Admit'] > 0.8]['CGPA'].mean())
print(graduate_admission[graduate_admission['Chance_of_Admit'] < 0.4]['CGPA'].mean())
#### Hrm, well, I guess one could have expected this. The GPA and GRE for students who have a higher chance of
#### being admitted, at least based on our cursory look here, seems to be higher.
## Pandas
Pandas is an open-source Python library for data manipulation and analysis, providing high-performance, easy-to-use data structures and data analysis tools.

Pandas is commonly used for working with structured data, such as tabular data, and offers functionalities for data cleaning, preprocessing, filtering, merging, and analysis, making it a powerful tool for data manipulation tasks in Python.
##
The main data structures provided by Pandas are
##
DataFrame: A DataFrame is a two-dimensional labeled data structure, similar to a table or a spreadsheet. It consists of rows and columns, where each column can hold different data types (numeric, string, datetime, etc.). DataFrames are useful for storing and manipulating structured data. They offer functionalities for indexing, selecting, filtering, merging, reshaping, and aggregating data.

Series: A Series is a one-dimensional labeled array that can hold any data type. It is similar to a column in a DataFrame or a single column of data. Series objects are useful for performing computations and operations on individual columns or data sequences. They also support indexing and slicing operations.

These data structures provide powerful capabilities for handling and analyzing data in a tabular format, allowing users to perform various data manipulation tasks efficiently.
### DataFrame Example:
import pandas as pd

### Creating a DataFrame from a dictionary
data = {'Name': ['John', 'Emma', 'Peter', 'Lisa'],
        'Age': [28, 32, 25, 30],
        'City': ['New York', 'London', 'Paris', 'Sydney']}
df = pd.DataFrame(data)

print(df)
###    Name  Age      City
0  John   28  New York
1  Emma   32    London
2 Peter   25     Paris
3  Lisa   30    Sydney
### Series Example:
import pandas as pd

### Creating a Series from a list
data = [10, 20, 30, 40, 50]
s = pd.Series(data)

print(s)
### 0    10
1    20
2    30
3    40
4    50
dtype: int64
## How to use API 
Using an API typically involves sending HTTP requests to a specific URL endpoint and receiving a response in a specified format, such as JSON or XML. Here are the basic steps to use an API
##
import pandas as pd
import requests
###
 Pandas provides powerful data manipulation and analysis tools, while Requests allows you to make HTTP requests to APIs. Here's an example that combines both libraries to fetch data from an API and process it using Pandas
###
response = requests.get('https://api.themoviedb.org/3/movie/top_rated?api_key=8265bd1679663a7ea12ac168da84d2e8&language=en-US&page=1')
###
It fetches the top-rated movies using the specified API key, language, and page parameters.
###
tem_dat=pd.DataFrame([response.json])
the JSON response from the API endpoint you provided contains multiple movie objects under the "results" key. If you want to create a DataFrame with each movie as a separate row, you can directly pass data['results'] to the pd.DataFrame() function without wrapping it in a list
###
for re in range(10):
    response = requests.get('https://api.themoviedb.org/3/movie/top_rated?api_key=8265bd1679663a7ea12ac168da84d2e8&language=en-US&page=1')
    tr=pd.DataFrame(response.json()['results'])[['id','title','overview']]
    df= tr.append(tr)
#### making a GET request to the "top_rated" endpoint of the "themoviedb" API in a loop. For each request, you are extracting specific data from the JSON response (movie id, title, and overview) and appending it to a DataFrame
##
## Bivariate
##
  mporting Libraries: The code begins by importing the necessary libraries, namely pandas and seaborn, using the import statement.

Loading Datasets: The seaborn.load_dataset function is used to load three datasets: 'tips', 'titanic', and 'flights'. These datasets are commonly used for demonstration purposes and come pre-packaged with the seaborn library.

Exploring the 'flights' Dataset: The flights.head() statement displays the first few rows of the 'flights' dataset, giving a glimpse of its structure and contents.

Scatter Plot: The sns.scatterplot function is used to create a scatter plot. It takes the 'total_bill' column as the x-axis, the 'tip' column as the y-axis, and assigns different colors (hue) based on whether the person is a smoker or not. Additionally, it differentiates the points by the gender (style) and sizes the points based on the party size (size).

Bar Plot: The sns.barplot function generates a bar plot. It visualizes the average 'Age' grouped by 'Pclass' (passenger class) on the x-axis, with the 'Age' values represented by the y-axis. The bars are further divided by the 'Sex' column (hue).

Box Plot: The sns.boxplot function creates a box plot. It shows the distribution of 'Age' for each gender (x-axis), split by the survival status (hue). The boxes represent the interquartile range, with the line inside representing the median.

Distribution Plots: The sns.distplot and sns.displot functions are used to create distribution plots. They display the distribution of 'Age' for two different groups based on the 'Survived' column. One plot shows the distribution for passengers who did not survive ('Survived' == 0), and the other plot shows the distribution for passengers who survived ('Survived' == 1). The distplot function shows a histogram and a fitted kernel density estimate, while the displot function provides a flexible interface for creating various distribution plots.

Kernel Density Estimation Plot: The sns.kdeplot function generates kernel density estimation plots. It visualizes the distribution of 'Age' for two groups based on the 'Survived' column. The hue is used to further differentiate the distributions based on 'Pclass'.

Cluster Map: The sns.clustermap function creates a clustered heatmap using the pd.crosstab function. It displays a matrix of counts showing the relationship between 'Parch' (number of parents/children aboard) and 'Survived' columns in the 'titanic' dataset.

Line Plot: The sns.lineplot function generates a line plot. It takes the 'year' column as the x-axis and the 'passengers' column as the y-axis, plotting the number of passengers over time.

Pivot Table Cluster Map: The final sns.clustermap function creates a clustered heatmap using a pivot table. It visualizes the relationship between the 'month' and 'year' columns from the 'flights' dataset, with the values being the number of passengers.  
##
## Grouping Data
##
Sometimes we want to select data based on groups and understand aggregated data on a group level. We have seen that even though Pandas allows us to iterate over every row in a dataframe, it is generally very slow to do so. Fortunately Pandas has a groupby() function to speed up such task. The idea behind the groupby() function is  that it takes some dataframe, splits it into chunks based on some key values, applies computation on those  chunks, then combines the results back together into another dataframe. In pandas this is referred to as the split-apply-combine pattern.
#
for group, frame in df.groupby('STNAME'):
    avg = np.average(frame['CENSUS2010POP'])
    print('Counties in state ' + group + 
          ' have an average population of ' + str(avg))
##
## Merging
##
In this lecture we're going to address how you can bring multiple dataframe objects together, either by merging them horizontally, or by concatenating them vertically. Before we jump into the code, we need to address a little relational theory and to get some language conventions down. I'm going to bring in an image to help explain some concepts.
this is a Venn Diagram. A Venn Diagram is traditionally used to show set membership. For example, the circle on the left is the population of students at a university. The circle on the right is the population of staff at a university. And the overlapping region in the middle are all of those students who are also staff.  Maybe these students run tutorials for a course, or grade assignments, or engage in running research experiments.

So, this diagram shows two populations whom we might have data about, but there is overlap between those populations.
When it comes to translating this to pandas, we can think of the case where we might have these two populations as indices in separate DataFrames, maybe with the label of Person Name. When we want to join the DataFrames together, we have some choices to make. First what if we want a list of all the people regardless of whether they're staff or student, and all of the information we can get on them? In database terminology, this is called a full outer join. And in set theory, it's called a union. In the Venn diagram, it represents everyone in any circle.

Here's an image of what that would look like in the Venn diagram.

![Union](merging2.png)
It's quite possible though that we only want those people who we have maximum information for, those people who are both staff and students. Maybe being a staff member and a student involves getting a tuition waiver, and we want to calculate the cost of this. In database terminology, this is called an inner join. Or in set theory, the intersection. It is represented in the Venn diagram as the overlapping parts of each circle.

Here's what that looks like: ![Intersection](merging3.png)

##
import pandas as pd

 First we create two DataFrames, staff and students.
 ####
staff_df = pd.DataFrame([{'Name': 'Kelly', 'Role': 'Director of HR'},
                         {'Name': 'Sally', 'Role': 'Course liasion'},
                         {'Name': 'James', 'Role': 'Grader'}])
####			 
 And lets index these staff by name
####
staff_df = staff_df.set_index('Name')
####
 Now we'll create a student dataframe
 #### 
student_df = pd.DataFrame([{'Name': 'James', 'School': 'Business'},
                           {'Name': 'Mike', 'School': 'Law'},
                           {'Name': 'Sally', 'School': 'Engineering'}])
 ####			   
 And we'll index this by name too
####
student_df = student_df.set_index('Name')
####
 And lets just print out the dataframes
#### 
print(staff_df.head())
####
print(student_df.head())
 ####
 #### If we want the union of these, we would call merge() passing in the DataFrame on the left and the DataFrame
#### on the right and telling merge that we want it to use an outer join. We want to use the left and right
#### indices as the joining columns.

pd.merge(staff_df, student_df, how='outer', left_index=True, right_index=True)
####
#### We see in the resulting DataFrame that everyone is listed. And since Mike does not have a role, and John
#### does not have a school, those cells are listed as missing values.

#### If we wanted to get the intersection, that is, just those who are a student AND a staff, we could set the
#### how attribute to inner. Again, we set both left and right indices to be true as the joining columns
pd.merge(staff_df, student_df, how='inner', left_index=True, right_index=True)
####
pd.merge(staff_df, student_df, how='left', left_index=True, right_index=True)
####
pd.merge(staff_df, student_df, how='right', left_index=True, right_index=True)
####
