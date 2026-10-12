# IT Asset Management System — ServiceNow

A ServiceNow application designed to manage the lifecycle of IT assets within an organization, from employee requests and manager approvals to allocation, maintenance, returns, retirement, and disposal.

## Project Overview

The IT Asset Management System helps organize and track IT equipment such as laptops, desktops, monitors, and mobile devices.

The application uses custom ServiceNow tables and automation to manage asset requests, assignments, maintenance activities, and returns.

It also includes access control configuration and references to Configuration Items in the ServiceNow CMDB.

## Objectives

- Manage IT asset inventory.
- Record and track employee asset requests.
- Support manager approval workflows.
- Automate asset allocation where an appropriate asset is available.
- Maintain asset assignment records.
- Manage maintenance and return activities.
- Track asset retirement and disposal.
- Configure role-based access controls.
- Link asset records to Configuration Items in the CMDB.

## Technology Stack

- Platform: ServiceNow
- Application Development: App Engine Studio
- Workflow Automation: Flow Designer
- Server-Side Logic: Business Rules
- Client-Side Validation: Client Scripts
- Security: Roles and Access Control Lists (ACLs)
- Scripting: JavaScript

## Application Modules

### 1. Asset

Stores asset information, including asset type, manufacturer, model, serial number, purchase details, assigned employee, status, and Configuration Item reference.

### 2. Asset Request

Manages employee requests for IT equipment, including the requested asset type, business justification, required date, manager, approval status, and request status.

### 3. Asset Assignment

Records the assignment of assets to employees and tracks assignment dates, expected return dates, and assignment status.

### 4. Asset Maintenance

Records maintenance activities, including maintenance type, issue description, technician, maintenance status, cost, and resolution.

### 5. Asset Return

Tracks asset returns, including the employee, return date, asset condition, return reason, and return status.

## Automation and Business Logic

The application includes the following implemented or configured components, subject to verification in the project instance:

- Manager approval workflow using Flow Designer.
- Automatic asset allocation workflow.
- Business Rules for assignment validation and asset lifecycle updates.
- Client-side validation for the required date.
- Role and ACL configuration.
- Asset-to-CMDB Configuration Item references.
- Email notifications, where configured.

## Workflow Overview

1. An employee submits an asset request.
2. The configured workflow initiates manager approval.
3. The request is approved or rejected.
4. For an approved request, the allocation flow searches for a suitable available asset.
5. If an asset is available, the flow updates the relevant records and creates an assignment record.
6. Maintenance and return modules support subsequent asset lifecycle activities.
7. Retirement and disposal records reflect the final stages of an asset's lifecycle.

Actual workflow behaviour depends on the configuration deployed in the ServiceNow instance.

## Screenshots

Project screenshots will be organized into the following categories:

- Application and tables
- Flow Designer
- Business Rules
- Client Scripts
- Security and ACLs
- ui policies

## Setup and Reproduction

This project was developed in a ServiceNow development instance.

To reproduce the application:

1. Set up a suitable ServiceNow development instance.
2. Create the scoped application and required custom tables.
3. Configure table fields, choice values, and reference fields.
4. Implement the required Flow Designer workflows.
5. Configure Business Rules and Client Scripts.
6. Configure roles and ACLs.
7. Link asset records to the appropriate CMDB Configuration Items.
8. Test the workflows and verify the resulting records.

Where available, use supported ServiceNow application or update-set export and import procedures to transfer the configuration. Review the exported components and test compatibility before using them in another instance.

## Testing

Testing should cover:

- Asset request creation and submission.
- Manager approval and rejection.
- Asset allocation when a matching asset is available.
- Behaviour when no suitable asset is available.
- Assignment record creation.
- Required date validation.
- Asset maintenance and return workflows.
- Access permissions for the configured roles.
- Asset-to-CMDB references.

Only tests verified in the development instance should be reported as successful.

## Author

Divya G.

B.Tech — Computer Science and Systems Engineering

## Project Purpose

Developed as an educational project to learn ServiceNow application development, workflow automation, server-side scripting, access control, and asset lifecycle management.
