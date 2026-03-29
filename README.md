# Excel IT Infrastructure Project Dashboard

Project Overview

In this project I built an Excel dashboard to track a small IT infrastructure setup.

The aim was to simulate how tasks are managed and monitored in a real IT environment, using something simple but still realistic.

The project includes tasks such as:

• Active Directory setup
• DNS and DHCP configuration
• User account creation
• Network setup and testing

The focus was on tracking progress, assigning work, and getting a clear overview of how the project is moving.

Project Structure

The workbook is split into two main sheets:

Tasks
Dashboard

The Tasks sheet holds all the raw data and calculations.

The Dashboard is where that data is summarised and visualised, so it’s easier to understand at a glance.

Tools and Features Used

• Microsoft Excel
• Tables
• Formulas
• Data Validation (dropdown lists)
• Pivot Tables
• Slicers
• Pie Chart

Tasks Sheet Setup
Creating the Task Table

I created a structured table to store all project data:

• Task ID
• Task Name
• Assigned To
• Start Date
• End Date
• Duration
• Status
• % Complete
• Priority
• Risk

Each row represents a task, and each column tracks a specific part of that task.

This acts as the central dataset for everything in the dashboard.

Duration Calculation

To calculate how long each task takes, I used:

=[@End]-[@Start]
Why this works

Excel stores dates as numbers in the background, so subtracting one date from another returns the number of days between them.

What this does

This means I don’t have to manually calculate durations. If I change a start or end date, the duration updates automatically.

Data Validation (Dropdown Lists)

To keep the data clean and consistent, I used dropdown lists.

Status

• Completed
• In Progress
• Not Started

Priority / Risk

• Low
• Medium
• High

How I added them
Selected the column
Went to Data → Data Validation
Chose List
Entered the values
Why I used this

Without dropdowns, it’s easy to enter slightly different values (e.g. “complete” vs “Completed”), which would break formulas and summaries.

Using lists ensures everything stays standardised and reliable.

Dashboard Sheet
Pivot Table (Task Progress)

I created a pivot table to summarise task progress.

Setup:

• Rows → Task Name
• Values → % Complete (Average)

Why I used average

If I summed percentages, the result wouldn’t make sense (it could go over 100%).

Using average gives a more accurate view of how complete each task is.

What this does

It lets me quickly see the progress of each task without scanning the full table.

Slicers (Filters)

I added slicers for:

• Status
• Assigned To

Why I used slicers

They make the dashboard interactive.

Instead of manually filtering the table, I can click a button to:

view only tasks in progress
check what a specific person is working on

This makes the dashboard quicker and easier to use.

Status Summary Table

I created a small table to count how many tasks fall into each status:

Status	Count
Completed	
In Progress	
Not Started	
Formulas used
=COUNTIF(G:G,"Completed")
=COUNTIF(G:G,"In Progress")
=COUNTIF(G:G,"Not Started")
Why I used this

The raw data isn’t suitable for charts directly.

This step converts it into a simple summary that can be visualised.

It also updates automatically whenever the task statuses change.

Pie Chart (Project Overview)

I created a pie chart using the summary table.

Why I used this

It gives a quick visual breakdown of the project:

• how much is completed
• what is still in progress
• what hasn’t been started

This is useful for reporting, where you want a quick overview rather than detailed data.
