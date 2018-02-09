# Slant Coders
*Clara Mohri, Kashf Mashrafi, John Liu*

*Lab 00 -- But What Does the Data Say?*

**Background:**


We are searching through a square matrix of dimensions n x n to find a value, and if it exists, return its' coordinates in the matrix. This matrix increases from left to right throughout rows, and increases from top to bottom throughout columns. 

**Algorithm Summary:**


Our search algorithm begins on the bottom left corner of the matrix.                                
Then, it compares our search val to the val found here. 
If the val found here is greater than our search val, then we look at the position one up. 
If the val found here is less than our search val, then we look at the position one to the right. 
Repeat the above two steps until the value is found.
If the row counter or column counter must be changed to something out of range, then the search val is not in our matrix, and we will return "(-1, -1)". 

**Hypothesis:**


The run-time efficiency of our algorithm for a matrix of of n rows (and therefore also n columns, because it is a square) is O(n).

**Experiment Methodology:**

We created a method called gen(int n) in MatrixFinder, that randomly generates a matrix of dimensions n * n that follows the previously mentioned standards. 
In our driver class, we experimented with the size of the matrix, going from 1,000 up to 10,000 by increments of 500. We randomly generated a number, and searched for this number in the randomly generated matrix a number of times, through our for-loop. The time in milliseconds was recorded right before find(matrix, number) was called, and also recorded right after the method was called. The difference was added to a sum, which was then divided by the number of trials, so as to find the average run time. 
To make sure that we weren't testing the best- or worst-case matrix, every 100 trials, we generated a new matrix to search. 
We tested the run time for different sizes by changing the size variable in the driver class. We also tested the run time based on the number of trials, by changing the value that i goes up to in our driver class.
We also tested on three different computers, knowing that run time can be different for different computers.

**Results:**

![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Chart0.jpg)

**Conclusions:**
