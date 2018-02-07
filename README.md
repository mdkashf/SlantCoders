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

**Results:**

**Conclusions:**
