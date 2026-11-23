# Contact Center Solution with ERP, API & CRM Integration | Banking

> **DUBAI CHARITY:**
> 1) As an Agent I want to be able to Upon receiving a reply from the department, the agent will be notified as the agent's email address is included in the CC field of the email. This will inform the agent that a response has been received from the department regarding the ticket concern. 10. In response, the agent will review their email inbox and proceed to close the ticket by adding their comments. During the closure process, there should be a provision to send the ticket closure email to the customer, if needed. So that Customer will be notified
Priority : High
Module : Idle
Sub Module : Email
Description : Upon receiving a reply from the department, the agent will be notified as the agent's email address is included in the CC field of the email. This will inform the agent that a response has been received from the department regarding the ticket concern. 10. In response, the agent will review their email inbox and proceed to close the ticket by adding their comments. During the closure process, there should be a provision to send the ticket closure email to the customer, if needed.

2) As an Admin I want to be able to An email should be triggered whenever the ticket's priority changes to "critical," which will be indicated by a red color. Once the initial email is sent, the department's data will be stored in the Convox database. Subsequently, Convox will send a reminder email to the same department email address So that Deparment will be notified
Priority : High
Module : Omnichannel
Sub Module : Tickets Settings
Description : Timeline priority change for the ticket • 24 hours then reminder for the regarded department if no answer came • 48 hours make it critical and should send an answer at least expect time to resolve the issue. • The priority of the complaint itself is related to the type of complaint and the desired department.

3) As an Agent I want to be able to the ticket details and its associated number will be sent to the respective department's email address. Additionally, the email address of the agent who initiated the process will be included in the CC field of the email. So that Deparment will be notified
Priority : High
Module : On Call
Sub Module : Email
Description : 4- Email Address for the departments

4) As an Agent I want to be able to the ticket details and its associated number will be sent to the respective department's email address. Additionally, the email address of the agent who initiated the process will be included in the CC field of the email. So that Deparment will be notified
Priority : High
Module : On Call
Sub Module : Email
Description : 4- Email Address for the departments

5) As an Agent I want to be able to Once the agent creates a ticket, a unique identification number for the ticket will need to be sent to the customer's mobile number and email address. This should follow the given template format. So that customer will be intimitated properly
Priority : High
Module : On Call
Sub Module : Email
Description : Once the agent creates a ticket, a unique identification number for the ticket will need to be sent to the customer's mobile number and email address. This should follow the given template format.

6) As an Admin I want to be able to After obtaining the necessary information from the customer, the agent will proceed to raise a ticket to the appropriate department. The agent will decide which department is better suited to address the issue. So that I can assing ticket to a specific department
Priority : High
Module : Omnichannel
Sub Module : Tickets Settings
Description : Name of All Departments • Projects Management department. • Customer Service department. • Orphans department • Resources development department. • Corporate Identity department • Information Technology department • General Aids department • Medical Aids department • Financial department • Partnerships department • Human resources department • Inventory department • Warehouse department • Purchase department • Management • Awareness and Education Department • Marketing department

7) As an Agent I want to be able to Whenever a customer contacts Dubai Charity to file a complaint or raise any kind of query, a contact center agent will receive the inbound call from the customer. The agent will record all the information provided by the customer regarding the complaint or query So that The ticket will be created with only the columns i need
Priority : High
Module :
Sub Module : Tickets Settings
Description : Employee name Type of complaint Complaint description Name of customer phone E-mail Department
> Tera Software:

1) Customer is requesting for the ticketing module for the city corporation.

2) City corporation branch

3) when the tera software raise a ticket for city corporation they should receive the ticket information and should be able to edit or reopen or close the ticket with comments and ticket update should receive to tera software in realtime.

4) we have to setup the new dashboard for the city corporation and ticketing module.

5) we need to link the tera software convox with the city corporation ticketing system for the real time update.

6) We have to create a supervisor login for the City corporation ltd to take any actions on the tickets raised.

7) for the stake holders new access will be provided to ticketing module system.

## Overview
Implementation of a contact center software solution for a public-sector bank,
integrated with the bank's ERP and CRM through APIs, supporting 350 users.
As Business Analyst, I owned requirements, documentation, API validation and
UAT from discovery to go-live.
M         /var/www/convox_perl/convox_leads_load_api.pl
M        /var/www/convox_perl/convox_leads_load_azure.pl
M        /var/www/convox_perl/convox_leads_load_spon.pl
M       /var/www/convox_perl/convox_leads_processing_azure.pl
M        /var/www/convox_perl/convox_leads_processing_spon.pl
M        /var/www/convox_perl/convox_web_leads_load_azure.pl
M        /var/www/convox_perl/convox_web_leads_load_spon.pl
M        /var/www/convox_perl/convox_web_leads_processing_azure.pl
M        /var/www/convox_perl/convox_web_leads_processing_spon.pl
M        /var/www/html/ConVoxCCS/rest/api.php

## Business problem
- Contact center, CRM and ERP data lived in separate systems
- Agents lacked a single view of the customer during calls
- Call outcomes and status were not reliably updated in the CRM
- Management had limited visibility into call and agent performance

## My role and responsibilities
| Phase | What I did |
| Discovery | Ran stakeholder workshops, mapped the as-is process, captured pain points |
| Requirements | Wrote the BRD and FRS, user stories and acceptance criteria |
| Design | Created BPMN / Lucidchart flows for the to-be process and integration points |
| API validation | Tested call-status, data-upload and click-to-call APIs in Postman |
| Testing | Planned and ran functional, integration, regression and UAT cycles |
| Delivery | Tracked defects and sprint work in JIRA, gave status reports to stakeholders |
| Adoption | Supported go-live and user onboarding for 350 users |

## Solution architecture
```
Agent Desktop / Contact Center
        |
   API layer (call status, data upload, click-to-call)
        |
   CRM  <------>  ERP
        |
   Reporting (SQL Server / Power BI)
```

## Key requirements delivered
- **FR-01** Click-to-call from the CRM record
- **FR-02** Automatic call-status update back to the CRM
- **FR-03** Bulk customer data upload into the dialer
- **FR-04** ERP data lookup during a live call
- **FR-05** Management dashboards for call and agent KPIs

## User story
> As a contact center agent, I want to call status to sync to the CRM
> automatically, so that I don't have to update records manually after
> every call.
>
> **Acceptance criteria**
> - Given a completed call, when the dialer sends the status, then the CRM
>   record updates within `10` seconds
> - Given an API failure, then the error is logged and retried

## Testing approach
- **Functional:** test cases per requirement, with traceability to the BRD
- **API:** Postman collection with positive, negative and boundary cases
- **Integration / Regression:** end-to-end flow checks after each release
- **UAT:** business sign-off with defect triage in JIRA

## Outcomes
- Went live for **350 users**
- `Implemented Successfully and resolved the agent manual intervention in the Salesforce CRM by 35%`
- `Lightning Version SLDS 1 and SLDS 2 support - UAT Demonstration - In 2 week Timeframe delivered the lightning solution`

## Tools used
`SQL Server` `Postman` `JIRA` `Lucidchart` `BPMN` `Power BI` `Excel` `SharePoint`

## Key learnings
- Writing clear acceptance criteria for integrations cut rework during UAT
- Validating APIs early surfaced data-mapping issues before UAT

## Contact
Syed Abdul Amer · [LinkedIn](https://www.linkedin.com/in/syed-abdul-amer-a840b3aa)
