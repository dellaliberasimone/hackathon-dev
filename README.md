# Developers Hackathon 🧑‍💻👩‍💻
Welcome to the Developers Hackathon. The goal is to develop a software described in the "Goal" section using the most modern development tools: Azure DevOps Repos/Pipeline for code and automation, GitHub Codespaces as development environment and obtaining assistance from GitHub Copilot.

## Prerequisites ✅
- Azure DevOps Repository

## Codespace Environment 💻
**Installed Software:** .NET 8, SQL Server 2019  
**VS Code Extensions:** GitHub Copilot, C#, SQL Server 2019

**SQL Server Connection**: Server: localhost,1433 - Username: sa - Password: P@ssw0rd  
**Connection string:**  Server=localhost,1433;User Id=sa;Password=P@ssw0rd;Database=OpticianApp;MultipleActiveResultSets=true;Encrypt=False

## Start the Hackathon 🏁
1) Replace <YOUR_ADO_REPO_CLONE_URL> and <YOUR_ENTRA_ID_TENANT_ID> placeholder in '.devcontainer/devcontainer.json' with the infomation of the repository in your Azure DevOps organization
2) Click on 'Code->New with options' and select a machine size to start the Codespace, wait for the inizialization and log-in to you Azure DevOps Tenant when prompted
3) Happy coding 😊

# Goal: Opticians App 🕶️

The basic workflow of the Application would be as follows:  
	• Opticians log into the system and enter customer data such as name, age, contact information, etc. This data gets stored in the Azure SQL Database.  
	• Opticians can then enter prescription data for each customer - details of their eye check-up, prescribed glasses/lenses, etc. This data is also stored in the Azure SQL Database.  
	• The app service then retrieves this data from the database and presents it in a user-friendly format. Opticians can view, update or delete the data as required.  

Functional requirements for the Customer Prescription Management System would include:

1. User Interface:
   - The system is a WebApplication and should have an intuitive, user-friendly interface.
2. Customer Management:
   - The system should allow opticians to add new customers into the system.
   - The system should allow opticians to view, update, and delete customer data.
   - The system should validate customer data input (e.g., check the format of email addresses).
3. Prescription Management:
   - The system should allow opticians to add prescription details for each customer.
   - The system should allow opticians to view, update, and delete prescription details.
   - The system should allow opticians to search prescriptions based on various parameters like customer name, prescription date, etc.
4. Reporting:
   - The system should allow opticians to export data in various formats (e.g., PDF, Excel).
5. Performance:
   - The system should be able to handle multiple concurrent users without performance degradation.
   - The system should load data quickly and efficiently.
6. Integration:
   - The system should integrate smoothly with the Azure SQL Database for data storage.
   - The system should integrate with Azure App Service for hosting and scaling the web application.
7. User Authentication:
   - The system should provide a secure login interface for opticians.

# GitHub Copilot assistance 🤖
Given the application requirments, try to ask to GitHub Copilot for help, following some suggestions:
<table>
	<tr><th>Requirements</th><th>Ask to GitHub Copilot…</th></tr>
	<tr>
		<td>The system is a WebApplication and should have an intuitive, user-friendly interface.</td>
		<td>Generate a .NET web application</td></tr>
	<tr>
		<td>Customer Management: <br>
		- The system should allow opticians to add new customers into the system. <br>
		- The system should allow opticians to view, update, and delete customer data. <br>
		- The system should validate customer data input (e.g., check the format of email addresses). <br>
		</td>
		<td>
		1. Generate a model a Customer with following data: ID, Name, Surname, Address, BirthDate, Mail, Phone  <br>
		2. Add NuGet packages for Entity Framework  <br>
		3. Generate Razor Pages for Create, Read, Update, and Delete by using scaffold tool for model Customer  <br>
		4. Add EF Initial database schema  <br>
		</td>
	</tr>
	<tr>
		<td>Prescription Management: <br>
		- The system should allow opticians to add prescription details for each customer. <br>
		- The system should allow opticians to view, update, and delete prescription details. <br>
		- The system should allow opticians to search prescriptions based on various parameters like customer name, prescription date, etc. <br>
		</td>
		<td>
		1. Generate a model for optical prescriptions associated to a Customer <br>
		2. Generate Razor Pages for Create, Read, Update, and Delete by using scaffold tool for model optical prescriptions <br>
		3. Add EF migration for optical prescription <br>
		4. Add search to prescription. Allow to search for customer name and prescription date to prescription <br>
		</td>
	</tr>
	<tr>
		<td>
		Reporting: <br>
		- The system should allow opticians to export data in various formats (e.g., PDF, Excel). 
		</td>
		<td>
		1. Export customer in excel and pdf<br>
		2. Export prescription in excel and pdf
		</td>
	</tr>
</table>
 
