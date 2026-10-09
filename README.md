# ACME Performer — UiPath REFramework

A UiPath RPA project that automates the retrieval, processing, and reporting of work items from a UiPath Orchestrator queue using the Robotic Enterprise Framework (REFramework).

## Overview

This project implements the Performer component of an RPA workflow. It retrieves queued transactions from UiPath Orchestrator, collects the transaction data into a DataTable, exports the complete DataTable to an Excel file, and sends the generated report via email.

The project follows the REFramework structure to organize initialization, transaction retrieval, processing, exception handling, and application cleanup. It also uses separate workflows for Chrome, email, Excel, and DataTable operations to keep the automation modular and maintainable.

## Key Features
* **Queue Integration:** Retrieves transaction items from a designated UiPath Orchestrator queue.
* **Transaction Processing:** Processes queued items using the REFramework transaction-processing mechanism.
* **DataTable Management:** Stores and organizes transaction information in a DataTable for structured data handling.
* **Excel Automation:** Exports the complete DataTable to an Excel workbook for reporting and further analysis.
* **Email Automation:** Sends the generated Excel report as an email attachment.
* **Modular Workflow Design:** Separates Chrome, email, Excel, and DataTable operations into dedicated folders and reusable workflows.
* **REFramework Structure:** Uses framework components to manage initialization, transaction processing, status updates, exception handling, and application cleanup.
  
## Workflow Overview

1. **Initialize:** Load configuration settings and prepare the automation environment.
2. **Retrieve Transactions:** Fetch transaction items from the designated Orchestrator queue.
3. **Process Transactions:** Read and process the retrieved queue items according to the workflow requirements.
4. **Build DataTable:** Collect transaction information and organize it into a structured DataTable.
5. **Export to Excel:** Write the complete DataTable to an Excel file.
6. **Send Email:** Send an email with the generated Excel report attached.
7. **Close Applications:** Complete the application cleanup process and finalize execution.

## Project Structure

```text
ACME Performer REFramework/
├── Chrome/
│   └── Chrome-related workflows
├── Email/
│   └── Email sending workflows
├── Excel/
│   └── Excel report generation workflows
├── DataTable/
│   └── DataTable creation and manipulation workflows
├── Framework/
│   ├── InitAllApplications.xaml
│   ├── InitAllSettings.xaml
│   ├── GetTransactionData.xaml
│   ├── Process.xaml
│   ├── SetTransactionStatus.xaml
│   └── ...
├── Tests/
│   └── REFramework test workflows
├── Main.xaml
├── project.json
├── project.uiproj
└── README.md
```


Note: The folder descriptions above are placeholders for the workflows in each folder. Update them with the actual .xaml filenames in your project if you want to document the structure in greater detail.

## Technologies and Tools

* UiPath Studio
* UiPath REFramework
* UiPath Orchestrator
* UiPath Queues and Transactions
* DataTable and Data Manipulation
* Excel Automation
* Email Automation
* Configuration-based Workflow Management
  
## Prerequisites

To configure and run this project, you need:

* UiPath Studio with compatible project dependencies.
* Access to a UiPath Orchestrator folder containing the designated transaction queue.
* The required queue items available for processing.
* A locally configured Data/Config.xlsx workbook, if required by the project's configuration.
* The necessary permissions and configuration for Excel file creation and email sending.
* A configured email account or email integration supported by the project's workflows.

Ensure that the queue name, output Excel file path, email settings, and other required values match your local environment before execution.

## Security Considerations

* Avoid hardcoding email passwords, access tokens, or other sensitive credentials in workflow files.
* Use secure credential storage and appropriate Orchestrator assets when credentials are required.
* Do not commit configuration files containing sensitive information or environment-specific secrets.
* Review generated Excel reports and email recipients to ensure that transaction data is shared only with authorized recipients.
* Before publishing the project, review workflow files and screenshots for credentials, tokens, personal information, or other sensitive data.

## Project Goal

This project demonstrates practical RPA development skills, including Orchestrator queue integration, transaction processing, structured data management, Excel report generation, email automation, reusable workflow design, and exception handling within the REFramework architecture.
