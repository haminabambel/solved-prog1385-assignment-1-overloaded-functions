Download Link: https://assignmentchef.com/product/solved-prog1385-assignment-1-overloaded-functions
<br>
Write a program that uses overloaded functions to assess individual student grades. Each time through the program’s main loop, it takes in a string that is in one of four forms:

<ul>

 <li>a single numerical grade as a floating point number that represents the student’s final mark (ranging from 0.0 to 100.0)</li>

 <li>a letter grade that is one of the following: A+, A, B+, B, C+, C, D, F, I, Q, AU, DNA, I/P – again that represents the student’s final grade</li>

 <li>from one to five numerical grades that are integers that represent the student’s mark on each of five assignments worth 20% each, separated by spaces (the marks range from 0 to 100).</li>

</ul>

Sample input might be :

<ul>

 <li>80 70 65 80 60 &gt;&gt;&gt; which results in a final grade of 71.00 %  o 80 90 50                 &gt;&gt;&gt; which results in a final grade of 44.00%</li>

</ul>

<ul>

 <li>a single character, ‘X’, that indicates that the user wants to exit the program</li>

 <li>Please note that this is <strong><u>not</u></strong> a menu-based program. That is, you are not to ask the user what type of grade they want to enter.  You must take their input and determine what type of input they specified.  This means <u>you need to develop a function which intelligently parses their</u> <u>input</u> to determine if they have entered a single double value, a single letter grade or from 1 to 5 integers.  There is an executable that you can play with (in the <em>Parse-And-Validate.zip</em> file) that might help you figure it out.</li>

</ul>

The string will be analyzed to determine if the student passed, failed, or had a special situation. If the student passes or fails, display a line that gives the numerical value of the mark and an indication as to whether the student passed or failed. A mark of 54.50% or higher is required in order to pass.  Your program’s output should look like this:

Student achieved ###.## % which is a PASS condition.   <strong><u>or</u></strong> Student achieved ###.## % which is a FAIL condition.




<u>Important Notes:</u>

<ul>

 <li>The two lines above will be the only allowed output from your program with the exception of o Special Situations (as noted below)

  <ul>

   <li>Any error messages that you need to output from your program</li>

  </ul></li>

 <li>Also note that in all input cases (the final grade, the letter grade and the assignment marks) – the program will output the grade as a floating point number (up to 2 decimal places)</li>

 <li>When testing your program I will only include valid input (i.e. a floating point number, an acceptable alpha-only input and a set of 1 to 5 integer values). Where o an acceptable floating point number may be “5” or “12500.6” or “-12.76” o an acceptable alpha-only input may be “A+”, “I/P” or “Hello” o an acceptable set of integers may be “1 2 3”, “673 -23 70 30 20”</li>

 <li>This means that I will not test with data like the following. It also means that you do not have to check for input given like this o I will not test with data like “6A.4”, “10 20 30 40 50 60 70”, “a+”, “50 A+ 30 45.2”, …</li>

 <li>In no input’s case will there be any trailing spaces so your solution should not depend on having trailing spaces</li>

 <li>If you see the need to create and add more functions to the solution – to properly modularize your solution design feel free to do so. A goal of every assignment, besides satisfying the requirements – is good design.  As we discussed in SEF last term, please make sure that your new functions exist in the appropriate source module(s).</li>

</ul>

Special situations are denoted by the letter grades as follows:

<table width="0">

 <tbody>

  <tr>

   <td width="105"><strong>Letter Grade</strong></td>

   <td width="266"><strong>Meaning</strong></td>

  </tr>

  <tr>

   <td width="105">I</td>

   <td width="266">Incomplete</td>

  </tr>

  <tr>

   <td width="105">Q</td>

   <td width="266">Withdrawal after drop/refund date</td>

  </tr>

  <tr>

   <td colspan="2" width="371">AU                     Audit</td>

  </tr>

  <tr>

   <td width="105">DNA</td>

   <td width="266">Did Not Attend</td>

  </tr>

  <tr>

   <td width="105">I/P</td>

   <td width="266">In Process</td>

  </tr>

 </tbody>

</table>

If there is a special situation, then the output would show the information as follows:

Student has Special Situation :  AU (Audit Condition)

For display purposes, the numerical equivalents for the letter grades are:

<table width="0">

 <tbody>

  <tr>

   <td width="101">Letter Grade</td>

   <td width="113">Numerical Equivalents</td>

  </tr>

  <tr>

   <td width="101">A+</td>

   <td width="113">95</td>

  </tr>

  <tr>

   <td width="101">A</td>

   <td width="113">85</td>

  </tr>

  <tr>

   <td width="101">B+</td>

   <td width="113">77</td>

  </tr>

  <tr>

   <td width="101">B</td>

   <td width="113">72</td>

  </tr>

  <tr>

   <td width="101">C+</td>

   <td width="113">67</td>

  </tr>

  <tr>

   <td width="101">C</td>

   <td width="113">62</td>

  </tr>

  <tr>

   <td width="101">D</td>

   <td width="113">57</td>

  </tr>

  <tr>

   <td width="101">F</td>

   <td width="113">50</td>

  </tr>

 </tbody>

</table>

<h1>What to Do</h1>

You must create three overloaded functions called assessGrade(). They will differ in their parameter lists:

<ul>

 <li>One will take a single parameter (char *) containing a letter grade or special situation.</li>

 <li>One will take a single parameter (double) containing the final mark.</li>

 <li>One will take five integer parameters containing assignment marks (or an array of five integers).</li>

</ul>

Review Module-01 for an understanding of how overloaded functions rely on each other (remember the “worker bee”) and how to design a solution with overloaded functions.  This program is to be <u>written in C</u>, but the <u>source file extensions need to be </u><u>.cpp</u> when you save them (in order to invoke the C++ compiler in VS).

You will create and submit <strong><u>only the following files</u></strong>:

<table width="0">

 <tbody>

  <tr>

   <td width="24">•</td>

   <td width="128">assign1.cpp</td>

   <td width="487">contains the main loop requesting the user’s input and the call to parse  and determine the type of user input</td>

  </tr>

  <tr>

   <td width="24">•</td>

   <td width="128">assessGrade.cpp</td>

   <td width="487">contains the logic for the 3 overloaded functions</td>

  </tr>

  <tr>

   <td width="24">•</td>

   <td width="128">assessGrade.h</td>

   <td width="487">contains the prototypes for the 3 overloaded functions as well as any other defines or constants you may need</td>

  </tr>

 </tbody>

</table>


