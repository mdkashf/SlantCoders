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


The run-time efficiency of our algorithm for a matrix of n rows (and therefore also n columns, because it is a square) is O(n).

**Experiment Methodology:**

We created a method called gen(int n) in MatrixFinder, that randomly generates a matrix of dimensions n * n that follows the previously mentioned standards. 
In our driver class, we experimented with the size of the matrix, going from 1,000 up to 10,000 by increments of 500. We randomly generated a number, and searched for this number in the randomly generated matrix a number of times, through our for-loop. The time in milliseconds was recorded right before find(matrix, number) was called, and also recorded right after the method was called. The difference was added to a sum, which was then divided by the number of trials, so as to find the average run time. 
To make sure that we weren't testing the best- or worst-case matrix, every 100 trials, we generated a new matrix to search. 
We tested the run time for different sizes by changing the size variable in the driver class. We also tested the run time based on the number of trials, by changing the number of iterations in our driver class.
We also tested on three different computers, knowing that run time can be different for different computers.

**Results:**

*Chart0:* 


![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Chart0.jpg)


This represents the data collected by Thinker 0 on their computer. 

*Chart1:*


![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Chart1.jpg)


This represents the data collected by Thinker 1 on their computer. 


*Chart2:*


![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Chart2.png)


This represents the data collected by Thinker 2 on their computer.



**Analysis:**


Although the data was collected on three different computers, the overall trend was decreased overall average runtime for more trials, and a linear increase in overall average runtime for greater size arrays. 
Furthermore, the data appears to be more regular for more trials; the 10 trial lines have much more variation than the 10,000 trial lines. The coefficients of determination approached 1 as the number of trials went up.
Below, we have isolated the 10,000 trial data to show that it greatly resembles a linear relationship. 
![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Linear0.png)
![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Linear1.png)
![alt text](https://github.com/mdkashf/SlantCoders/blob/master/Linear2.png)



**Conclusions:**


Our hypothesis of having O(n) runtime for arrays of n x n appears to be supported by our data. For the 10,000 trial lines, which were the most regular, lines of best fit can be drawn and are linear. Furthermore, the coefficients of determination approached one, so we can say that this data was linear.
Something that we do not know how to explain is why the average runtime decreased for greater trial number so significantly. One possible explanation could be that it has to do with the way that Java is first compiled and then executed.

