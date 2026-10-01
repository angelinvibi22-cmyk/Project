**Project Overview:**

This project establishes an automated solution for importing bulk structured employee data from external spreadsheets into ServiceNow using Import Sets and Transform Maps. The system stages raw spreadsheet data in a staging table, maps source fields to custom target table fields, and uses Coalesce logic to update existing entries while preventing duplicate record creation. Integrated reporting and dashboards provide visual insights into department distribution, location counts, and data integrity.

ParameterConfiguration DetailSource ReferenceStaging Table Label / NameEmployee Import (u_employee_import)Target Table Label / NameEmployee Test (u_employee_test)Transform Map NameSample Spreadsheet ImportCoalesce KeyEmployee ID (u_employee_id)Dashboard NameEmployee Analytics Dashboard

**Execution Phases & Implementation :
**
Steps:

Phase 1: Data PreparationCreate a Google Spreadsheet populated with sample employee attributes: Employee ID, Name, Email, Department, and Location.   Export and save the spreadsheet locally in Excel format (Sample Spreadsheet.xlsx).  

Phase 2: Target Custom Table CreationNavigate to Tables > Create New.   Set Label to Employee Test and Name to u_employee_test.   Access the form layout via Form Context Menu > Configure > Form Layout.   Add the following fields to the custom table:   Employee ID (Type: String)   Employee Name (Type: String)   Email (Type: String)   Department (Type: String)   Location (Type: String)   Click Save and verify fields render properly on the Employee Test form.   

Phase 3: Import Set Table SetupNavigate to System Import Sets > Load Data.   Select Create table and enter Label: Employee Import (system populates Name: u_employee_import).   Under Source of the import, select File and upload Sample Spreadsheet.xlsx.   Set Sheet number: 1 and Header row: 1, then click Submit.  

Phase 4: Transform Map Configuration & ExecutionClick Create Transform Map from the completion screen.   Set Name to Sample Spreadsheet Import, select Target table as Employee Test [u_employee_test], and verify Source table is set to Employee Import [u_employee_import].   Click Auto Map Matching Fields or use Mapping Assist to configure field alignments:   u_employee_id $\rightarrow$ u_employee_id   u_name $\rightarrow$ u_employee_name   u_email $\rightarrow$ u_email   u_department $\rightarrow$ u_department   u_location $\rightarrow$ u_location   Click Transform to transfer data into the target table.  

Phase 5: Initial Data ValidationOpen the Employee Test table list view from the Application Navigator.   Customize view order using Personalize List Columns to confirm all initial records imported accurately.

Phase 6: Coalesce ConfigurationNavigate to System Import Sets > Transform Maps and open Sample Spreadsheet Import.   In the Field Maps related list, locate u_employee_id and set Coalesce to true.   Save the form.  

Phase 7: Re-import Validation & Upsert OperationsPrepare an updated Excel sheet containing 4 rows:   2 existing employee IDs with modified names/emails (e.g., updating email for SB-0010 and name for SB-0004).   2 new employee records (SB-0016 and SB-0017).   Navigate to System Import Sets > Load Data, select Existing table (Employee Import), attach the updated spreadsheet, and click Submit.   Click Run Transform.   Review Transform History to verify processing metrics:   Total Records: 4   Inserts: 2 (New employees)   Updates: 2 (Existing employees updated via Coalesce match)   Ignored: 0   Re-run the import using the exact same file to verify duplicate prevention logic:Total Records: 4   Inserts: 0   Updates: 0   Ignored: 4   

Phase 8: Analytical Reports SetupNavigate to Reports > Create New under Usage and Governance and build three reports:   Employees by DepartmentType: Pie Chart   Table: Employee Test [u_employee_test]   Group By: Department   Aggregation: Count   Employees by LocationType: Bar Chart   Table: Employee Test [u_employee_test]   Group By: Location   Aggregation: Count   Employee List ReportType: List   Table: Employee Test [u_employee_test]   Columns Displayed: Employee ID, Employee Name, Email, Department, Location  

Phase 9: Dashboard IntegrationEnsure ACL settings permit pa_dashboards creation for admin overrides.   Navigate to Self-Service > Dashboards or access PA_DASHBOARDS.FORM.   Create a new dashboard named Employee Analytics Dashboard.   Open each report created in Phase 8, click Share > Add to Dashboards, select Employee Analytics Dashboard, and confirm positioning. 

**Project Outcomes:**

Data Automation & Integrity: Successfully automated spreadsheet data migration into ServiceNow staging and custom target tables.   Duplicate Prevention: Implemented Coalesce matching on Employee ID to perform seamless upsert operations, preventing record duplication on recurring imports.  
Operational Analytics: Consolidated real-time departmental and geographic data visualizations into a single dashboard for centralized monitoring.   
<img width="1934" height="867" alt="image" src="https://github.com/user-attachments/assets/f4b8326e-d7af-418d-88d3-65336f6e65b3" />
<img width="1915" height="934" alt="image" src="https://github.com/user-attachments/assets/d7ed2d3b-ea9c-4e93-8cd8-c3611199609f" />











