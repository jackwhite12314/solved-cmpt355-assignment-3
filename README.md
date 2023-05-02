Download Link: https://assignmentchef.com/product/solved-cmpt355-assignment-3
<br>
<strong>Part 1 – Requirements Gathering: /30</strong>

In the next meeting with our contact at GNBC they have provided us with the data files from one of their existing vendors. They have files for the employee data, job data, department data, and location file.




After reviewing their current data, they have added some specifications to our new database. They need to maintain all the employee personal data they have right now, such as the full name, birthdate, marital status, and home email. There is also the employee’s employment status (e.g. if the employee is on leave, suspended, etc) that was previously neglected. Additionally, they’ve noted that they need to keep track of their employee’s performance review records over time. The latest performance review information is contained in the employee file. Finally, there is more information about the employee’s job assignment that needs to be addressed. Standard hours is the number of hours the employee is expected to work in this job. They can be in a Permanent (Regular) or Temporary position. There is also the distinction of whether or not their job assignment is part-time, full-time, or casual.




File descriptions




<u>Employee File</u>

This is the main information file from the vendor. This is a flat file including all the information relating to the employee.




<u>Job File</u>

This file contains a listing of the available jobs in the company.




<u>Department File </u>

This file contains the department information for the company, including the department supervisor job code. Jobs in the executive department supervise the majority of these departments. However, the banking departments are supervised by individual branch managers. For example, the banking department in Saskatoon is supervised by the Branch Manager in Saskatoon and the banking department in Calgary SE is supervised by the Branch Manager in Calgary SE, whereas all the financial services departments across the company are supervised by the VP of Finance.




<u>Location File</u>

This file contains the location information for the company.




<strong>Part 2 – Create a Load Procedure: /30</strong>

The vendor will be sending these files nightly in order to keep our system synced with theirs. You need to write repeatable pl/pgsql code that will add/update the required information in your database every time a new file is sent. You should load the given files (as shown in the first tutorial), and use your load procedure to populate your database accordingly. You should make sure that you are doing appropriate validation and error handling. You shouldn’t rely on any triggers for this assignment.




Tip: It’s helpful to create load tables to import in the initial datafile for further manipulation. Then you can select from your [load_employees] table in your load procedure to insert the data into appropriate tables in your database.




Tip: Remember that in reality data files are rarely perfect. You may run into issues and it is generally up to you to overcome these issues, or at the very least identify them and come up with possible solutions.

<strong> </strong>

<strong>Part 3 – Analysis /30</strong>

<u>Reports/Queries /15</u>

<ol>

 <li>Create a report of all active employees consisting of the following fields: employee number, employee name (formatted lastname, firstname), birthdate, gender, current length of service (number of years the employee has been active), job title, length of time in current job, department, location, pay type, pay amount, supervisor name, last performance rating text. Note: the length of service should not be calculated with the original hire date if the employee is a rehire. ‘s</li>

 <li>Create a report of the top performing active employee in each department in the company. Your report should include the employee name (formatted lastname, firstname), performance rating number, performance rating text, performance rating date, current length of service.</li>

 <li>Create turnover reports (reporting on terminated employees).

  <ol>

   <li>An individual report consisting of the employee name (formatted lastname, firstname), employee age, termination date, most recent length of service, termination type, and termination reason.</li>

   <li>An aggregate report of terminated employees from each department, consisting of the department code, the department name, the number of terms, the percentage of terms in this department as compared to number of terms overall.</li>

   <li>A report of the number of terms for each job in the company, ordering the results by the job with the highest to lowest turnover. The report should consist of the job title, job code, and number of terms.</li>

  </ol></li>

</ol>

<u>Review /15</u>

<ol>

 <li>Explain what changes you made to your database in Part 1 and why.</li>

 <li>Were there any issues you ran into with loading the data file in Part 2? This may include the data itself, constraints (or lack thereof), formatting, etc. Explain how you overcame these issues.</li>

</ol>

<strong> </strong>

<strong>Part 4 – Style /10</strong>

<strong> </strong>

<strong> </strong>

<strong>What to hand in:</strong>

<strong>Part 1</strong>

<ol>

 <li>A new ER diagram of your database that reflects the updated structure of your database, along with the diagram you handed in for assignment 2. This new diagram can be simply created in DB Visualizer instead of being created like in assignment two. The point is for the marker to be able to easily see what changes have been made.</li>

 <li>One .sql file with the DDL script you used to change your database for these requirements.</li>

</ol>




<strong>Part 2</strong>

<ol>

 <li>Script files of all functions/procedures that you made for your nightly load.</li>

</ol>

<strong> </strong>

<strong>Part 3</strong>

<ol>

 <li>One sql file with all of the queries you used for your reports. Remember to comment which question you are answering before the query itself.</li>

 <li>One .txt file with your responses to the questions.</li>

</ol>