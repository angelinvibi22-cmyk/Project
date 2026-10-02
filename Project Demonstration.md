**1. Introduction**

Good morning everyone. Today I am going to demonstrate my project titled “Import Data Using Transform Maps” in ServiceNow.

The main objective of this project is to import employee data from an Excel spreadsheet into ServiceNow using Import Sets and Transform Maps.

This project also includes Coalesce to prevent duplicate records, along with Reports and Dashboards for analyzing employee information.

**2. Employee Table and Import Set**

First, I created a custom table called Employee Test, which is the target table for storing employee information.

The table contains five fields: Employee ID, Employee Name, Email, Department, and Location.

Next, I created an Import Set table called Employee Import. This table acts as a staging area where employee data from the Excel spreadsheet is initially loaded.

**3. Transform Map and Data Import**

Next, I created a Transform Map named Sample Spreadsheet Import.

The source table is Employee Import, and the target table is Employee Test.

I mapped the source fields to their corresponding target fields using field mapping. After saving the Transform Map, I executed the transformation.

ServiceNow transferred the employee records from the Import Set table to the Employee Test table. I then verified that the records were successfully imported.

**4. Coalesce and Duplicate Prevention
**
Next, I implemented Coalesce in the Transform Map using Employee ID as the identifying field.

Coalesce helps ServiceNow identify existing employee records during repeated imports.

When an existing Employee ID is imported with updated information, the corresponding record can be updated instead of creating a duplicate. New Employee IDs are inserted as new records.

I verified the results using Transform History.

**5. Reports and Dashboard**

Next, I created three reports using the Employee Test table.

Employees by Department: Displays employee distribution by department using a Pie Chart.

Employees by Location: Displays employee distribution by location using a Bar Chart.

Employee List Report: Displays employee details, including Employee ID, Name, Email, Department, and Location.

Finally, I created a dashboard named Employee Analytics Dashboards and added all three reports to it.

This dashboard provides a centralized view of employee information.

**6. Conclusion
**
To conclude, this project demonstrates how ServiceNow can import and manage employee data efficiently using Import Sets and Transform Maps.

Coalesce helps prevent duplicate records, while Reports and Dashboards make employee information easier to analyze.

This completes my project demonstration.

https://drive.google.com/file/d/1xRb8gll9w4ErVE5AO7XGz_-3YoMVAd7w/view?usp=sharing
