The attachment contains the following files

Data Collection

	T-SQL Scripts

	CREATEDATABASE, CREATEOBJECTS & CREATECOLLECTIONJOB -> these t-SQL script creates the database dba_local & schema & SQL Agent Jobs required for performance data collection. These SQL scripts needs to be ran on all the sql instance which needs to be monitored

	Powershell  Scripts 

	Get-SQLPerfCounters, Out-DataTable, Write-DataTable -> These Powershell scripts needs to be copied to location C:\Scripts\ which is used for Perfmon data collection. These script needs to be copied  on all the target server which needs to be monitored & should be copied to the folder C:\Scripts


SQL Performance baselining Reports & Xevent Reports (SSRS Reports)

	The SSRS Reports should be deployed on the central SSRS server which should be greater than SQL 2012.


You can follow the steps mentioned below  to set it up in your environment. 

Data Collection Steps for each SQL Instance to Monitor

1.	Connect to SQL instance to monitor
2.	Run CREATEDATABASE.sql
3.	Run CREATEOBJECTS.sql
4.	Run CREATECOLLECTIONJOB.sql
5.	Copy PS Scripts in the folder C:\Scripts
6.	Check SQL Agent JOBs History to see if it runs successfully
7.	Repeat for each SQL Instance you want to monitor

Setting up & Deploying Reporting  

8.	Deploy the SSRS Reports & see if data populates in the reports.

