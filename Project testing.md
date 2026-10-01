Report 1: Employees by Department

Data tab

Field	Content
Report name	Employees by Department
Source type	Table
Table	Employee Test [u_employee_test]

This exactly matches the project instructions: the first report is named “Employees by Department”, uses Table as the source type, and uses the Employee Test table.

Then click Next / Type and enter:

Type
Chart type: Pie
Click Next
Configure
Group by: Department
Aggregation: Count
Click Next

These are the specified settings for the Employees by Department report.

Style
<img width="1911" height="703" alt="image" src="https://github.com/user-attachments/assets/39dc7b03-fb3c-49d7-a554-a11f4ce6cf75" />
Enter/keep these settings
Field	What to select
Group by	Department
Additional group by	Leave empty
Display data table	Leave unchecked
Configure function field	Leave unchanged
Aggregation	Count
Set Value Formatting	Leave unchanged
Max number of groups	System Default
Show Other	Keep checked

Your screenshot already has the important project settings correct: Group by = Department and Aggregation = Count. The project specifically requires these two settings.

What the screen should look like

Configure

Group by
┌─────────────────────────┐
│       Department ▼      │
└─────────────────────────┘

Additional group by
┌─────────────────────────┐
│                         │
└─────────────────────────┘

☐ Display data table

Aggregation
┌─────────────────────────┐
│          Count ▼        │
└─────────────────────────┘

Set Value Formatting

Max number of groups
┌─────────────────────────┐
│     System Default ▼    │
└─────────────────────────┘

☑ Show Other

             [ Next ]
Then

Click Next → you will go to the Style section.

For Style, your project says to leave the chart color as default, then click Run and Save.
<img width="1906" height="861" alt="image" src="https://github.com/user-attachments/assets/3766eeec-f0b6-442d-b878-997c692a82f8" />

Enter/keep these settings
Style option	What to select
General	Keep selected
Chart color	Use color palette
Set palette	Default UI14
Display data labels	Leave unchecked
Custom chart size	Leave unchecked
Chart size	Large
Drilldown view	Leave empty
Decimal precision	2
Your current screen

Your screenshot already shows the correct default-style configuration:

✅ Chart color: Use color palette
✅ Palette: Default UI14
✅ Display data labels: unchecked
✅ Custom chart size: unchecked
✅ Chart size: Large
✅ Drilldown view: empty
✅ Decimal precision: 2

The pie chart is also displaying the department counts, such as ServiceNow, Salesforce, and Aiml, based on the data currently in your Employee Test table.

What to do next

At the top-right:

Run → check the report → Save

Your project specifically says to leave the chart color at default, then Run and Save the report.

Final result

Your Employees by Department report will be:

Report Name: Employees by Department
Table: Employee Test [u_employee_test]
Chart: Pie
Group By: Department
Aggregation: Count
Style: Default

After saving this, you can move on to Report 2 – Employees by Location.
<img width="1910" height="893" alt="image" src="https://github.com/user-attachments/assets/5c611889-2b39-4ba5-92a4-d8158205b351" />






Leave the chart color as Default
Click Run
Click Save
