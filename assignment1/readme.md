<html>
<head>
</head>
<body>
<h1>COMP 250 Winter 2015 Assignment 1 Instructions</h1>
<p>Version 1.0 16 January 2015</p>
<p><strong>DUE MONDAY 2 FEBRUARY 11pm</strong></p>
<h2>Background</h2>
<p>In this assignment you will implement a tool called <i>Proffinder</i>. This tool is a mini search engine to help you find a professor that works in a specific area that matches your interests. Proffinder will work by downloading the webpage of a professor and determining how similar it is to a query that consists of keyword (such as {"programming", "software", "engineering"}).</p>
<p>In addition to practicing the concepts seen in class to date, this assignment will expose you to web scraping, to some of the main ideas in <a href="http://nlp.stanford.edu/IR-book/">information retrieval</a>, and to the research areas of the professors in the School of Computer Science.</p>
<p>In this assignment, documents will be modeled as arrays of Strings, where each String is a word in the document (with duplicates). However, we will remove <i>stop words</i> from documents. These are words, like <i>the</i>, that do nothing to help us estimate similarity.</p>
<p>To estimate the similarity Sim(D,Q) between a document D and a query Q, we will use two different measures: the <a href="https://en.wikipedia.org/wiki/Jaccard_index">Jaccard index</a>, and a home-grown measure we will call RelHits. The Jaccard index is the intersection of the query and a document (with duplicates removed) divided by the union of the query and document. RelHits will be defined as the number of times any query keyword is found in a document divided by the total number of words in the document.</p>
<h4>Examples</h4>
<pre>DOC = {armadillo, camel, cat, cat, dog, dog, goat, the, tiger, tiger}
DOC_NO_STOP_WORDS = {armadillo, camel, cat, cat, dog, dog, goat, tiger, tiger}
QUERY = {camel, tiger}
SIM_JACCARD = 2/6 = 0.33
SIM_RELHITS = 3/9 = 0.33

DOC = {a, design, design, design, engineering, the, theory, testing}
DOC_NO_STOP_WORDS = {design, design, design, engineering, theory, testing}
QUERY = {graphics, testing}
SIM_JACCARD = 1/5 = 0.20
SIM_RELHITS = 1/6 = 0.17
QUERY = {design}
SIM_JACCARD = 1/4 = 0.25
SIM_RELHITS = 3/6 = 0.50
</pre>
<p>The processing of web pages will be handled by a special library called <a href="http://jsoup.org/">jsoup</a>, so you don't have to worry about the details. The library should be automatically linked to your project once you import the assignment 1 package as described below</p>
<h2>Requirements</h2>
<p>You may be able to make the project work on other environments, but we will support the following cross-platform configuration:</p>
<ul>
<li>Eclipse Luna</li>
<li>Java 7</li>
</ul>
<h2>Instructions</h2>
<ol>
<li>Enroll into a mycourses group as soon as possible, and no later than Wednesday 21 January 4pm. After that assignments will be assigned to groups and if you are not in a group you will not be able to submit your assignment. You must enroll yourself into a group even if you want to work alone.</li>
<li>Download the assignment 1 package and import it into Eclipse (File -&gt; Import -&gt; General -&gt; Existing Projects into Workspace). The code skeleton should build without errors. Run the main method to make sure everything works.</li>
<li>Read the academic integrity statement at the bottom of this page and paste it into the header of file Assignment1.java intended for this purpose.</li>
<li>Complete the code provided as part of the assignment package. All further instructions are in the source code comments.</li>
<li>Submit your answer as a single file called <tt>Assignment1.java</tt> that contains the academic integrity statement and all your solution. Do not submit a zip file, class files, or any other kind of artifact besides that single file. The file you submit should at the very least compile without any errors.</li>
</ol>
<p>Upload a single solution file per group by <strong>Monday 2 Feb 11:00pm</strong>. Assignments submitted between 11:01pm and 7:00am the next day will receive a -40% absolute penalty. It will not be possible to submit assignments after Tuesday 3 Feb 7am. Clear and fixed deadlines ensure fairness and speedier feedback.</p>
<h2>Important Tips for Managing Your Time</h2>
<ul>
<li>Poor performance in assignments is generally the result of bad time management as opposed to incomprehension of the material. Plan your time carefully.</li>
<li>Import the file and make sure everything works right away. If there is a problem you will have plenty of time to ask for help and calmly solve the issue. Do not wait to discover that you have a configuration problem close to the deadline.</li>
<li>Work incrementally and test your solution often. Start with the more basic functions. Do not try to do a so-called "big bang integration" where everything is supposed to come together nicely in the end (because it probably won't).</li>
<li>Bugs are normal and learning to solve them is part of this course. However, make sure to plan for them by allocating the necessary time. Do not expect that everything will work as it should right away.</li>
<li>We have set up the submission site to allow resubmissions. You can and should submit early, as soon as you have something reasonable. You will be able to upload new versions of your work until the deadline. However, if you have something pretty good submitted on time, don't override it after the deadline as you will instantly lose 40%.</li>
<li>If you are doing this assignment with a partner, we recommend trying to work on the solution together at the same time, using a technique called <a href="https://en.wikipedia.org/wiki/Pair_programming">pair programming</a>.</li>


</body>
</html>
