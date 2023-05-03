Download Link: https://assignmentchef.com/product/solved-cs1331-homework-05-water-fountain
<br>



<strong> </strong>

<h1>Problem Description</h1>

The water fountain company that you work for wants to re-write the code for their water fountains. The production team has given you all the information that needs to be tracked by each water fountain. The sales team has also given you a few requirements for special features to help sell the updated models. Your job is to make a Java class to represent a water fountain that contains all the information and requirements you have received. Unfortunately, you are the only software developer at your job so you have to write everything yourself.

<h1>Solution Description</h1>

For this assignment create a file named WaterFountain.java. You will have to fill in the required instance variables and methods listed below.

<strong>Instance Variables:</strong>

<ul>

 <li>String modelName

  <ul>

   <li>modelName should have private access and be used to hold the model name of the water fountain • boolean requiresMaintenance</li>

   <li>requiresMaintenance should have private access and be used to hold if the water fountain requires maintenance or not.</li>

  </ul></li>

 <li>int cupsPoured

  <ul>

   <li>cupsPoured should have private access and be used to hold the number of cups of water the water fountain has poured.</li>

  </ul></li>

</ul>

<strong>Static Variable:</strong>

<ul>

 <li>int totalWaterFountains

  <ul>

   <li>totalWaterFountains should have private access and be used to hold the number of water fountains that have been created. It should be set to 0 by default.</li>

  </ul></li>

</ul>

<strong>Constant Variable:</strong>

<ul>

 <li>String SOFTWARE_VERSION

  <ul>

   <li>SOFTWARE_VERSION should have public access, not be able to be changed, and should be able to be referenced statically. The variable should be set to “2.0.0”.</li>

  </ul></li>

</ul>

<strong>The Constructor:</strong>

The constructor should only take in values for modelName and cupsPoured and set each of them respectively. requiresMaintenance should be initialized to false and totalWaterFountains should be incremented by one.

<strong>The Methods:</strong>

All getters and setters should have public access.

<ul>

 <li>Proper Getter &amp; Setter for modelName</li>

 <li>Proper Getter &amp; Setter for requiresMaintenance</li>

 <li>Proper Getter &amp; Setter for cupsPoured</li>

 <li>Proper Static Getter for totalWaterFountains</li>

 <li>void pourCup()

  <ul>

   <li>This method takes no parameters, returns nothing, and has public access. If the water fountain does not require maintenance, cupsPoured should be incremented by one. If the water fountain does require maintenance, do nothing.</li>

  </ul></li>

 <li>boolean equals(WaterFountain other)

  <ul>

   <li>This method takes in a WaterFountain, returns true if the other passed in water fountain is logically equal to this water fountain and false otherwise, and has public access. Water fountains are logically equal if they have the same modelName, cupsPoured, and SOFTWARE_VERSION.</li>

  </ul></li>

 <li>String toString()

  <ul>

   <li>This method takes no parameters, returns a String, and has public access. This method will return a string that contains the water fountain’s modelName, requiresMaintenance, cupsPoured, and SOFTWARE_VERSION.</li>

   <li>If the water fountain needs maintenance the returned string should match this: “[modelName] has poured [cupsPoured] cups, requires maintenance, and is running version: [SOFTWARE_VERSION]”</li>

   <li>If the water fountain does not need maintenance then the returned string should match this: “[modelName] has poured [cupsPoured] cups, does not require maintenance, and is running version: [SOFTWARE_VERSION]”</li>

   <li>Example: “A-222 has poured 987 cups, does not require maintenance, and is running version: 2.0.0”</li>

  </ul></li>

</ul>

<strong>Note: Each method requires proper JavaDocs (see below for more information)</strong>

<h1>Testing your code</h1>

If you want to test out your own code before submitting we recommend creating a separate java file and implementing a main method there. You can then create new water fountains and test your methods. Below is some sample testing code. <strong>These tests are not comprehensive!</strong>

WaterFountain wf = new WaterFountain(“A-222”, 987) WaterFountain wf2 = new WaterFountain(“B-5”, 1) wf.toString()

-&gt; A-222 has poured 987 cups, does not require maintenance, and is running version: 2.0.0 wf.pourCup() wf.getCupsPoured()

-&gt; 988 wf.equals(wf2) -&gt; false wf.equals(wf)

-&gt; true

WaterFountain.totalWaterFountains

-&gt; 2

Feel free to create your own tests in the main method! Try to write tests for the remaining methods in the file!

<h1>Rubric</h1>

<ul>

 <li>[15] Method Variables

  <ul>

   <li>[5] Correct visibility and type for instance variables</li>

   <li>[5] Correct visibility, modifiers, and type for totalWaterFountains</li>

   <li>[5] Correct visibility, modifiers, and type for SOFTWARE_VERSION</li>

  </ul></li>

 <li>[20] Constructor

  <ul>

   <li>[15] Correct setting of instance variables</li>

   <li>[5] Increments totalWaterFountains</li>

  </ul></li>

 <li>[20] Getters &amp; Setters

  <ul>

   <li>[5] Correct Getter &amp; Setter for modelName</li>

   <li>[5] Correct Getter &amp; Setter for requiresMaintenance</li>

   <li>[5] Correct Getter &amp; Setter for cupsPoured</li>

   <li>[5] Correct Getter for totalWaterFountains</li>

  </ul></li>

 <li>[10] Correct pourCup() method</li>

 <li>[20] Correct equals(WaterFountain other) method</li>

 <li>[15] Correct toString() method</li>

</ul>

<strong>Allowed Imports</strong>

To prevent trivialization of the assignment, you are <em>not </em>allowed to import any classes or packages.

<h1>Feature Restrictions</h1>

There are a few features and methods in Java that overly simplify the concepts we are trying to teach or break our auto grader. For that reason, do not use any of the following in your final submission:

<ul>

 <li>var (the reserved keyword)</li>

 <li>exit</li>

</ul>

<h1>Javadocs</h1>

For this assignment, you will be commenting your code with Javadocs. Javadocs are a clean and useful way to document your code’s functionality. For more information on what Javadocs are and why they are awesome, the <a href="http://www.oracle.com/technetwork/java/javase/documentation/index-137868.html">online overview</a> for them is extremely detailed and helpful.

You can generate the javadocs for your code using the command below, which will put all the files into a folder called javadoc:

$ javadoc *.java -d javadoc

The relevant tags that you need to include are @author, @version, @param, and @return. Here is an example of a properly Javadoc’d class:

<strong>import </strong>java.util.Scanner;

<em>/**</em>

<ul>

 <li>This class represents a Dog object<em>.</em></li>

 <li><strong>@author </strong>George P<em>. </em>Burdell</li>

 <li><strong>@version </strong><em>0</em></li>

</ul>

<table width="632">

 <tbody>

  <tr>

   <td width="632"><em>*/ </em><strong>public class </strong>Dog {<em>/**</em>* Creates an awesome dog <em>(</em>NOT a dawg<em>!)</em><em>*/ </em><strong>public </strong>Dog() { …}<em>/**</em>* This method takes in two ints and returns their sum* <strong>@param a </strong>first number* <strong>@param b </strong>second number <em>* </em><strong>@return </strong>sum of a and b<em>*/ </em><strong>public </strong>int add(int a, int b) {…}}</td>

  </tr>

 </tbody>

</table>

A more thorough tutorial for Javadocs can be found <a href="https://cs1331.gitlab.io/cs1331-style-guide.html">here</a>.

Take note of a few things:

<ol>

 <li>Javadocs are begun with /** and ended with */.</li>

 <li>Every class you write must be Javadoc’d and the @author and @verion tag included. The comments for a class should start with a brief description of the role of the class in your program.</li>

 <li>Every non-private method you write must be Javadoc’d and the @param tag included for every method parameter. The format for an @param tag is @param &lt;name of parameter as written in method header&gt; &lt;description of parameter&gt;. If the method has a non-void return type, include the @return tag which should have a simple description of what the method returns, semantically.</li>

</ol>