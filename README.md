# Cost-Optimization-and-Monitoring-using-Microsoft-Azure
Cost Optimization and Monitoring
STEP 0:  Problem Background

Company “X” is an engineering company that has offices in both the US East & West Coast. They currently host all their data and applications in a single East coast data center and are constantly worried about both cost and resiliency. Below is how their current servers are configured.
Server(s): 	Purpose: Windows/Linux Server
Environment: Physical Servers
Operating System: Windows 
Operating System License: DataCenter
Servers: 10
Procs per server: 2
Core(s) per proc: 8 Cores
RAM: 256 GB
Optimize By: CPU
GPU: None
Usage: These are the servers where all your engineering workloads happen. Currently they all are being leveraged at regular capacity.
Server(s): 	Purpose: Web App
Environment: Physical Servers
Operating System: Windows 
Operating System License: DataCenter
Servers: 3
Procs per server: 1
Core(s) per proc: 8 Cores
RAM: 64 GB
Optimize By: CPU
GPU: None
Usage: These are the web app servers for your company. Currently they all are being leveraged at regular capacity.
Server(s): 	Source: Database Server 
Database: Microsoft SQL Server 
License: Enterprise
Environment: Physical Servers
Operating System: Windows 
Operating System License: Datacenter
Servers: 3
Procs per server: 1
Cores per proc: 16 Cores
RAM: 64 GB
Optimize By: CPU
Usage: These three servers are running Microsoft SQL Server and provide the database for your engineering company. It is critical that they are always running. 
Destination
Service: SQL Database
Purchase Model: vCore
Service Tier: Business Critical
Instance Cores: 2
SQL Server Storage: 5
SQL Server backup:  0     
Storage	Purpose: Storage
Type: Local Disk / SAN
Disk Type: HDD
Capacity: 1 TB
Back-Up: None currently
Archive: None
Networking 	Amount of network bandwidth you currently consume in your on-premises environment: 1 GB




 
STEP 1: Assessing the On-Premises Environment & Generating Total Cost of Ownership (TCO) Report 

Purpose: To identify the Azure services needed to ensure Company “X”’s business continuity in the cloud.

Current Environment/
Background

Make a list of all current on-premises servers and services.	There are 10 Windows VM’s which are used for engineering purposes.
There are 3 web apps servers which host the front end of the company. 
There are 3 database servers. 
There is a storage which is also used to store data.
Matching Azure Services

Match the list of on-premises servers and services to the corresponding Azure ones.	Make a list of all servers and services you would create on Azure and explain why you chose each. 

Hint:
●	For VM’s and Web Apps:  The operating system license is always Standard and Virtualization is always Hyper-V. 
●	For databases: The purchase model is vCore, the Service Tier is Business Critical, and no SQL Server Backup is needed.
●	For networking: The defaults of 200 GB for outbound bandwidth are used.
 
Screenshot 1

Submit the screenshot for each of the above configurations from Azure TCO. 
VM and Web Apps Server screenshot should be submitted here.	

Screenshot 2

Submit the screenshot for each of the above configurations from Azure TCO. 
Database screenshot should be submitted here.	

Screenshot 3

Submit the screenshot for each of the above configurations from Azure TCO. 
Storage configuration screenshot should be submitted here.	
Screenshot 4

Submit the screenshot for each of the above configurations from Azure TCO. 
Networking configuration screenshot should be submitted here.	
Screenshot 5

Once the TCO Report is generated, submit a screenshot of the price comparison graph (line graph) here.	



Screenshot 6

Once the TCO Report is generated, submit a screenshot of the price comparison graph (pie chart) here.	




Screenshot 7

Once the TCO Report is generated, submit a screenshot of the price comparison chart (tabular format) here.	

Explanation 1

Explain the breakdown of the costs and show your understanding of how on-prem costs versus Azure compare	


STEP 2: Azure Pricing Calculator Cost Estimates 

Purpose: You want to only move the engineering workloads (so just your VM’s) to Azure first to try and understand how Azure cloud works. In addition, this will also help you demonstrate to your CIO that by doing that small migration your company can achieve resiliency. You want to provide precise monthly costs to your CIO.

Use the Azure Pricing Calculator to submit the following screenshots.

Task 1
	Matching Azure Services: Match the list of on-premises servers and services to the corresponding Azure ones.

Here is the VM configuration you will pick.
●	5 VM’s will be in US East Coast, and 5 will be in US West Coast.
●	The instance will be B16MS in both regions (16 vCPUs, 64 GB RAM, 128 GB Temporary Storage, $0.73 per hour).
●	Compute Option will be pay-as-you-go; so, there are no upfront costs.
●	The default of 730 hours is selected. 
Screenshot 1

Submit the screenshot for each of the above configurations from the Azure Pricing Calculator. Submit the US East Coast monthly costs here.	

Screenshot 2

Submit the screenshot for each of the above configurations from the Azure Pricing Calculator. Submit the US West Coast monthly costs here. 	


Screenshot 3

Submit the screenshot for total cost per month for both US East and West Coasts. 
	

Explanation 1

Explain how resilience is built in by moving to Azure	
 
STEP 3: Azure Cost Management + Billing 

Background

	You have now configured your Azure Production Workload environment and been using Azure for a few days. You have now been tasked by your CIO to present some metrics on how the costs are being billed within Azure and also what other functionalities Azure has in regards to cost management, which were not previously available.
Question 1

Submit the explanation 	What is the purpose of Azure Cost Mgmt + billing Dashboard?
Explanation 1


	
Screenshot 2

Submit the screenshot for main Cost Mgmt + Billing Dashboard.  	Hint: Navigate to the Cost Management Section on the left and then click “Cost Analysis” to reach this dashboard. Students need to submit the main screenshot of the Billing dashboard 


Explanation 2

Explain the key components of the screenshot submitted. An explanation to be provided for
Scope and Area dropdown from the screenshot submitted. 	Hint: Make sure the right time period is selected to see the data. 



Screenshot 3

Submit the screenshot for breakdown of costs by Service Name and Location.	Hint: Navigate to Cost Management Section on the left, and then click “Cost Analysis” to reach this dashboard. These pie charts are under the above graph submitted. 


Explanation 3

Explain the key components of the screenshot submitted. 
	

Screenshot 4

Submit the screenshot for breakdown of costs by Service Name and Location.	Hint: Navigate to Cost Management Section on the left and then click “Cost Alert” to reach this wizard. Next, click on “Add button” on top left under this tab. This is Part 1 of the wizard (of the 2-part process).



Explanation 4

Explain the key components of the screenshot submitted. 
	
Screenshot 5

Submit the screenshot for breakdown of costs by Service Name and Location	Hint: This is Part 2 of the wizard (of the 2-part process).




 
Explanation 5

Explain the key components of the screenshot submitted. 
	

 
Screenshot 6

Submit the screenshot for breakdown of costs by Service Name and Location.	


 
Explanation 6

Explain the key components of the screenshot submitted. 
	
 
Explanation 7

Explain the summarized highlights of this part of the project, Azure Cost Mgmt + Billing 	





 


 
STEP 4: Azure Policy to create and enforce policies 

Background

	You have now configured your Azure Production Workload environment and been using Azure for a few days. You realize that many infrastructure administrators are creating VM sizes without doing proper due diligence, thus having a direct impact on cost. 

You now decide to leverage Azure Policy features to ensure that appropriate controls are put in place.
Screenshots 1 through 5

Submit the screenshots for Azure Policy steps.	Hint: Navigate to and select the built-in Azure policy “Allowed virtual machine size SKUs;” then follow the wizard steps. Submit a screenshot for every single step of the wizard so that any mistakes in the final step can be caught by your reviewer. 

Very important note: 
1.	Due to lab restrictions, while you go through the wizard,  you will not be allowed to create the policy in the final step. Please submit all screenshots though
2.	So for the Part 2 of this project to be submitted, a successful policy has already been created in the lab for you, which can be used to test the VM creation scenario. Please ensure to double check which VM series is allowed to be created in the lab and ensure that you do not use the same series for passing this part of the project 

Step 1:


Step 2:



Step 3



Step 4:




Step 5:



Screenshot 6

Explain through screenshots what happens when you create a VM which is in violation with the policy you just created. 
	Once the Azure policy creation is complete, try to create a VM which is of a “NOT ALLOWED” size. 

Hint: pick any size; it doesn’t matter as long as it's not in the allowed list in Azure policy you just created. 

Once you go through the wizard, in the final step you will see the following screenshot, which needs to be submitted.

 
Explanation 1

Explain the summarized highlights of this part of the project, Azure Policy. 	


STEP 5: Azure Dashboards

Background
	Azure Dashboards are a one stop shop to monitor
●	Your logs
●	Your infrastructure
●	Your applications 
Task 1	You need to create an Azure dashboard that will pull in a few widgets: Percentage CPU, All Resources, Resource Groups & Avg CPU Credits Consumed. Submit the screenshots and explain the key components of the Dashboard. Be sure to include a screenshot of the final Dashboard.
Screenshots1 through 3

You will submit the screenshots for Overview tab.	Step 1:



Step 2:



Step 3 (Final Output):




 
STEP 6: Azure Monitor – Metrics 

Task 1	You need to navigate to Azure Monitor > Metrics screen and create a Percentage CPU as a metric and submit screenshot of the graph generated and pin to dashboard.
Screenshots 1 through 3

You will submit the screenshots for Monitor | Metrics screen as you are setting up 	Step 1:



Step 2:



Step 3:


Screenshot 4

Now that Azure Metrics Monitor is configured, please set an alert for that metric. The alert is whenever the Avg % CPU is greater than 0.3; then the alert will be triggered.	



STEP 7: Azure Monitor – Log Analytics  

Task 1	You need to create a Log Analytics workspace and submit step-by-step screenshots.
Screenshots 1 through 4

You will submit the screenshots for Log Analytics workspace creation screens.	Step 1:



Step 2:



Step 3:



Step 4:




 
STEP 8: Azure Insights  

Background
	Azure Insights can only be created once you have the Log Analytics workspace completed.
Screenshots1 through 6

You will submit the screenshots for the Monitor | Metrics screen as you are setting up.	Hint 1: Navigate to Insights > Applications and then click Add button  
Hint 2: The Log Analytics workspace you created before will be used here

Step 1:



Step 2:



Step 3:



Step 4:



Step 5:


Step 6: Click “Go to resource”





Screenshots 7 through 12

You will submit screenshots of you enabling the VM.	Hint 1: So now that you have created Azure Insights for the Resource group, you need to go to Virtual Machines tab and actually enable it for the VM itself.

Hint 2: The key is to select the Log Analytics workspace which you created above in STEP 7:  Azure Monitor – Log Analytics.

Step 7:



Step 8:


Step 9:

Step 10:



Step 11:


Step 12: 




 
STEP 9: Azure Monitor – Smart Alerts   

Task 1	Navigate to Setup Alert & Actions under Azure Monitor >Overview.

The condition name should be CPU units consumed and its value should be greater than 0.3.
Screenshots 1 through 8

You will submit step-by-step screenshots for creating a Setup Alert & Actions. 	Step 1:



Step 2:



Step 3:



Step 4:



Step 5:



Step 6 (Summary after above steps):


Step 7 (Screenshot post-creation of the alert):


Step 8 (If you had any alerts, they would be submitted here):


Explanation 1

Explain the purpose of Azure Dashboards, Azure Monitor and alerts
	


 
STEP 10: Autoscale In-Out Based on Number of Users per CPU Core   

Task 1	The lab will have a Virtual Machine Scale set already created.
Navigate to Azure Monitor > Settings > Autoscale. 
You will create an Autoscale rule as part of this project. 
Screenshots 1-5

You will submit step-by-step screenshots for creating an autoscale rule under Azure Monitor.	Step 1 (Browse to Monitor > Autoscale):



Step 2 (Select the option for Custom autoscale and within that Scale based on metric and then click “Add Rule”):



Step 3 (Create the scale rule. They key part on this screen is that Percentage CPU metric is selected):




Step 4 (Once scale rule is created, submit the summary screenshot):


Step 5 (Screenshot for “Autoscale Enabled”):

Explanation 1

Explain the key details of autoscale screenshots you have submitted.	


