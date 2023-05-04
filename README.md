Download Link: https://assignmentchef.com/product/solved-cse-232-programming-project-1
<br>
<strong> </strong>

<h1>Assignment Overview</h1>

This project focuses on some mathematical manipulation. It is worth 5 points (0.5% of your overall grade). It is due Monday, September 10<sup>th</sup>   before midnight.




<h1>The Problem</h1>

Global warming discussions are a hot topic these days. A paper in early August 2018 called

“<u>Trajectories of the Earth System in the Anthropocene</u>” predicted that if the global temperature increase by 7 degrees Fahrenheit, the change would be irreversible. We are going to explore the change in global temperature versus year based on a simple linear model and make some predictions as to when this might occur.

<h2>Some Background</h2>

Hopefully you remember that a linear model is created by specifying a slope and an intercept where you can use the equation y = slope * x + intercept (y is the temp, x is the year). I gathered (see spreadsheet) the average global temp in degrees Fahrenheit, 1880-2012, and fit a linear model to it. The slope is 0.01173 degreesF/year and the intercept is 34.3491 degreesF. Using this information, you will write a program that does as follows.




<h1>Program Specifications</h1>

Your program will do the following:

<strong>1.</strong>Take as input two values:

<ol>

 <li>a year, as a long</li>

 <li>a slope, as a doublePrint three results:</li>

 <li>Print the <strong><u>temperature</u></strong> for the year read in above based on the slope and intercept provided in the Background section. Print it as a <strong>double</strong> of <strong>precision 2</strong>.</li>

 <li>Print the <strong>year</strong> when, given the temperature calculated in above, a temperature 7 degrees greater will occur again using the slope and intercept provided in the Background. Print it as a <strong>rounded long</strong>.</li>

 <li>Print the <strong>year</strong> when, given the temperature calculated in above, a temperature 7 degrees greater will occur using the second input, a new input <strong>slope, </strong>and the intercept provided in the Background. Print it as a <strong>rounded long</strong>.</li>

</ol>

<strong> </strong>

<strong>Deliverables </strong>proj01/proj01.cpp . The name of the directory is proj01, the name of the file you turn in should be exactly proj01.cpp in a directory named proj01. This is how all projects will be turned in: in a directory containing a file(s). To help with this, we will check that this is true  with the first test case in Mimir. Just like the lab, you must click on proj01 within “Project 01 – model of global warming” to submit the file. <strong>Not the file</strong> proj01.cpp, <strong>the directory</strong> proj01 in which the file proj01.cpp is contained.




<strong> </strong>

<strong>Assignment Notes: </strong>

<ol>

 <li>We might as well try to make the output somewhat readable. You can look this up in the text or on the internet, but you can use the following modifiers that affect how numbers print.

  <ol>

   <li>cout &lt;&lt; fixed;</li>

  </ol></li>

</ol>

Elements will be printed as floating point numbers (ex 123.456). <strong>Use this for the project.</strong>

<ol>

 <li>cout &lt;&lt; scientific;</li>

</ol>

Elements will be printed in scientific notation (ex 1.23456 x 10<sup>2</sup>). This is an alternative but <strong><em>not what we want</em></strong> for this project.

<ol start="123">

 <li>cout &lt;&lt; setprecision(2); Floating point numbers will have 2 values after the decimal point and will be rounded, (123.46). To make this work we need another include, and that is</li>

</ol>

#include&lt;iomanip&gt;

<strong><u>Provide the </u></strong><u>include<strong> and use </strong></u><u>setprecision(2)<strong> for this project.</strong></u>

<ol start="123">

 <li>Thus cout &lt;&lt; fixed &lt;&lt; setprecision(2) &lt;&lt; 123.4567 &lt;&lt; endl; will print 123.46</li>

</ol>

<ol start="2">

 <li>The following statement will read two variables off of the same, space separated line. It is an example of chaining input:</li>

</ol>

… long lng; double dbl; cin &gt;&gt; 1ng &gt;&gt; dbl;

…

You can also do it on separate lines. Your choice

… cin &gt;&gt; lng; cin &gt;&gt; dbl;

…

<ol start="3">

 <li>If you #include&lt;cmath&gt; you get access to the std::round The std::round function takes as an argument the number to be rounded and returns the nearest integral value (see <u>https://en.cppreference.com/w/cpp/numeric/math/round</u> for full details)</li>

 <li>There are 4 tests provided. The first is a file-exists test to make sure you got the directory issue correct, the remaining three are input-output tests.</li>

 <li>You <strong><em><u>do not</u></em></strong> have to check for bad input values. In general, we will explicitly indicate the errors we are looking for, but for now we are not checking for input errors.</li>

 <li>It gets irritating to type in 2 numbers every time you test. To get around this, you can use a handy trick off the command line. You can create a file with the 2 input values (on a single line, they need to be space separated, on 2 different lines is also fine). You can <strong><u>redirect</u></strong> the file to your main program. With that file in the same directory as the compiled out, you can do:</li>

</ol>




./a.out &lt; fileOfInput.txt




This will automatically feed the input to the cin statement and produce the output. Makes it easier to test things. An example input.txt is provided in the project directory.







<strong>Getting Started </strong>

<ol>

 <li>In Mimir, I create the directory proj01 and place in it an empty file (no contents) with the correct name, proj01. You can update the file contents there.</li>

 <li>If you are in a CSE lab (or whatever your environment), then bring up an editor and a terminal, create a project directory proj01 in your M: directory (or your local laptop) and create proj01.cpp within that directory.</li>

 <li>Write your code and compile it.</li>

 <li>Prompt for some of the values and print them back out, just to check yourself.</li>

 <li>Check that your calculations are right (as indicated above).</li>

 <li>In Mimir, create a directory proj01 and, within that directory, an empty proj01.cpp file.</li>

 <li>However you choose to do your development, the easiest way at this point to check yourself on Mimir is to copy and paste from your editor to the proj01 file on Mimir and submit.</li>

 <li>You don’t have to pass all the tests the first time! You can add more information and pass more of the tests as you progress. Do things incrementally.</li>

 <li>Now you enter a cycle of edit-run to incrementally develop your program.</li>

 <li>If a version you submit and test on Mimir passes all the tests, you are done. If time runs out and you didn’t pass all the tests, then however many you passed indicates what grade you got for the project. Though it doesn’t matter much now as this is relatively easy, at the end you do the best you can and pass as many tests as possible. However, <strong><em><u>you always know</u></em></strong> how you are doing and that is the advantage of Mimir.</li>

 <li><strong><em><u>Remember</u></em></strong>: In the end, it only matters that it compiles and runs on Mimir. If it doesn’t compile there, then it doesn’t compile at all (no matter what else you did on whatever environment you used). Mimir is the last word.</li>

</ol>