# Integrate-BigQuery-Data-and-Google-Workspace-using-Apps-Script


Challenge scenario
You are a junior cloud engineer assigned to a team. So far you have been helping your team create and manage Google Cloud resources.

For this lab, your challenge is to use Google Cloud's BigQuery API (as an Apps Script advanced service) and the built-in Apps Script services for Google Sheets to perform data analysis. In addition, you also need to create a Google Sheets spreadsheet and populate data into it, as well as create a chart with spreadsheet data.

You are expected to have the skills and knowledge to complete the tasks that follow.

Your challenge
In this lab, you are asked to:

Query BigQuery and log the results to a Google Sheets worksheet with Apps Script.
Connect a BigQuery dataset to Google Sheets.
Use Google Charts to visualize spreadsheet data with Connected Sheets.
Use Apps Script to create a new worksheet and populate it with data.

Task 1. Query BigQuery and log the results to Google Sheets
For this task, as a prerequisite for the steps that follow, you need to create a new Apps Script project by navigating to script.google.com and then rename the project to a name of your choice.
Solution :

Enter and run your application code
Copy the code in the box below and paste it over everything in the code editor:


Change the file name to bq-sheets.gs and press Enter.

Review the query code for the function runQuery():
Solution: Check the code.gs





Task 2. Perform calculations on charts with Connected Sheets

For this task, you need to analyze a public dataset containing data on taxi trips in Chicago. To start, open the Google Sheets home page.
Connect a BigQuery dataset to Google Sheets
Make the connection from new Blank Spreadsheet to BigQuery dataset.
Connect a BigQuery dataset to Google Sheets using Data connectors.
Select your Project ID qwiklabs-gcp-03-5c75185a9d46 > Public datasets > chicago_taxi_trips > taxi_trips.
Use formulas with Connected Sheets


Next, you can use different formulas with Connected Sheets.
1. Find out how many taxi companies there are in Chicago.
2. Find the percentage of taxi rides in Chicago that included a tip.
3. Find the total number of trips where the fare was greater than 0.


Solution:
1. =COUNTUNIQUE(taxi_trips!company)
   
2. =COUNTIF(taxi_trips!tips, ">0")
   
3. =COUNTIF(taxi_trips!fare, ">0")
4. =D1/E1




Task 3. Use Google Charts with Connected Sheets
For this task, you use Charts (in this instance, pie and line charts) to inspect popularity of rides and trends of payment types.

View the following information in Google Charts:

As a pie chart, what forms of payments are people using for their taxi rides?
As a line chart, how has revenue from mobile payments for taxi trips changed over time?
As a line chart, how have mobile payments changed over time since revenue peaked in 2015?
