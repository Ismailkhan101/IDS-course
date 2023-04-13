# Question 1
Write a function called proportion_of_education which returns the proportion of children in the dataset who had a mother with the education levels equal to less than high school (<12), high school (12), more than high school but not a college graduate (>12) and college degree.

This function should return a dictionary in the form of (use the correct numbers, do not round numbers):
#
The overall purpose of the code is to calculate the proportions of children in the dataset who have mothers with different education levels, and store the results in a dictionary. The dictionary has four key-value pairs, where the keys represent the education level categories and the values represent the corresponding proportions in the dataset. The code uses the pandas library to read the CSV file, calculate the value counts and proportions, and create the dictionary, which is then returned as the output of the function. The assertions at the end of the code are used to check that the function returns a dictionary with the correct keys and number of items.
