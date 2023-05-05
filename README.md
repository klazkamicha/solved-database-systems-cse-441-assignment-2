Download Link: https://assignmentchef.com/product/solved-database-systems-cse-441-assignment-2
<br>
In this assignment you have to implement the two­phase merge sort algorithm to sort large number of records.

<strong> </strong><strong>Algorithm Implementation: </strong>

<strong> </strong>You need to consider following points:

<ol>

 <li>The main memory to be used will be limited and specified by the input parameters.</li>

</ol>

For C/C++, use the dynamic memory allocation malloc and request 80% of the main memory specified in MB from the underlying OS and use the same memory for sorting. You

shouldn’t use array or global variable to allocate memory for the sorting variable.

For Java, use the argument ­Xmx to restrict the heap size equal to the memory specified in MB.

<ol start="2">

 <li>The metadata file will contain the information about the size of the different columns (in bytes).</li>

 <li>All the columns in the input file will be separated by a space.</li>

 <li>The datatype for the column will be string only.</li>

 <li>The number of columns can ranges from 1 to 100.</li>

 <li>You program should be capable of sorting in both ascending and descending order (based on argument given).</li>

 <li>Your program should run for different values of main memory allowed and different size of files ranging from MBs to GB s.</li>

</ol>

If we found your program is using main memory more than it is specified, you will lose marks.




<strong>Input Format: </strong>

<strong> </strong>

<strong>metadata.txt (</strong>considered in the same folder as your executable file) containing the information about the column size. &lt;column name 1&gt;,&lt;size of the column&gt;

&lt;column name 2&gt;,&lt;size of the column&gt;

&lt;column name 3&gt;,&lt;size of the column&gt;

……

&lt;column name n&gt;,&lt;size of the column&gt; <strong>input.txt </strong>

Containing the records with the column values separated by the space. All the values will be in the string only.




<strong>Command Line Inputs </strong>

<ol>

 <li>Input file name (containing the raw records)</li>

 <li>Ouput file name (containing sorted records)</li>

 <li>Main memory size (in MB)</li>

 <li>Order code (asc/desc) asc means to sort in ascending order and desc means to sort in descending order</li>

 <li>Columname1</li>

 <li>Columnname2</li>

 <li>…..</li>

</ol>

<strong>Example </strong>

<strong> </strong>

<table width="291">

 <tbody>

  <tr>

   <td width="24">●</td>

   <td width="48">./sort</td>

   <td width="219">input.txt output.txt 50 asc c0 c1</td>

  </tr>

  <tr>

   <td width="24">●</td>

   <td width="48">./sort</td>

   <td width="219">input.txt output.txt 100 desc c0</td>

  </tr>

  <tr>

   <td width="24">●</td>

   <td width="48">./sort</td>

   <td width="219">input.txt output.txt 100 asc c1 c0</td>

  </tr>

  <tr>

   <td width="24">●</td>

   <td width="48">./sort</td>

   <td width="219">input.txt output.txt 500 asc c2</td>

  </tr>

 </tbody>

</table>




As in the first example, the file input.txt to be sorted in ascending order with 50 MB space based on column c0 and if any column have same value for c0 then on the basis of c1, available. (Similar to ORDER BY clause in SQL).

In case if the value is same for all the available columns, then the order should be the same as in the input file.




<strong>Graph Generation: </strong>

<strong> </strong>

You have to generate two graphs:




<ul>

 <li>FileSize(X­axis) v/s Time(Y­axis)</li>

</ul>

Take the main memory size as 100 MB and run you alogrithm for file size 5MB, 50MB,

500MB, 1GB, 2GB, 3GB, 4GB and 5GB and note the time taken for each run. Plot the graph.




<ul>

 <li>Memory Size (X­axis) v/s Time (Y­axis)</li>

</ul>

Take a file of size 512MB and run your code with main memory argument as 10 MB, 25 MB,

100 MB, 250 MB, 512 MB and note the time taken for each run..

You can use any language or tool to plot the graph. (Matlab, Ms Excel). You will need to provide the matrix and the image file the graph.










<strong>Error Handling: </strong>

Check feasibility condition for two­way merge sort for provided memory constraints. If not satisfied, provide error message and halt. In this case, the output.txt should not generated.

<strong> </strong>

<strong>Test Data: </strong>

To generate input file, visit <u>http://www.ordinal.com/gensort.html</u> and download <strong>gensort</strong> code to generate data.




The following command generates the first 100 tuples of three columns. $&gt; ./gensort ­a 100 input.txt




To validate your algorithm you can use the <strong>valsort</strong> available on the same link.