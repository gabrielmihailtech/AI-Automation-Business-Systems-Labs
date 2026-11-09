# Lab 02 – Automation Solution Design

**Project:** Purchasing Automation – Business Systems & AI  
**Lab Type:** Workflow Design and Business Requirements  
**Environment:** Simulated Manufacturing Company  
**Status:** Completed – Conceptual Design Only

---

## 1. Scenario

Westbridge Manufacturing Ltd. is a fictional Irish manufacturing company that currently manages purchasing requests through emails, Excel spreadsheets and manual ERP operations.

During Lab 01, several operational inefficiencies were identified, including incomplete purchasing requests, repeated communication, delayed approvals, duplicate requests and limited visibility of purchasing activities.

Management has requested a proposed automation solution using existing Microsoft technologies without replacing the ERP system.

## 2. Objective

Design a structured purchasing request workflow that improves data accuracy, reduces unnecessary communication and maintains appropriate management approval and purchasing controls.

The proposed design should consider data validation, duplicate requests, delivery tracking and potential integration limitations.

## 3. Original Exercise Requirements

### Task 1 – Approval Design

Determine how management approval should be handled within the proposed purchasing request process.

Consider how approval can be verified and documented.

### Task 2 – Data Validation

Identify mandatory fields and validation rules required before a purchasing request can be submitted.

### Task 3 – Duplicate Prevention

Explain how the proposed system should identify or prevent potentially duplicate purchasing requests.

### Task 4 – Request Tracking

Define suitable request statuses to support purchasing visibility and operational monitoring.

### Task 5 – Exception Handling

Evaluate the following scenarios:

1. A purchasing request is submitted without genuine management approval.
2. Two employees request identical components for the same project.
3. A supplier delivers only part of the ordered quantity.

Propose practical controls for each scenario.

---

## 4. Proposed Automation Solution

### 4.1 General Workflow

The proposed process begins with the employee discussing material requirements directly with the department manager.

The employee and manager review the component list, quantities and project details together.

Only an authorised manager can submit the purchasing request through Power Apps using their Microsoft 365 account.

The request is stored in SharePoint and made available to the Purchasing Administrator.

The administrator verifies the request, checks existing purchasing records and creates the Purchase Order in the ERP system.

Power Automate could be used to notify Purchasing when a new request is submitted.

### 4.2 Approval Verification

Management approval is represented by the authorised manager submitting the request through their own Microsoft 365 account.

The application should verify the user's identity and submission permissions.

Recording the manager's identity and submission timestamp would provide an audit trail.

The system should not rely solely on a manually entered manager name or an unverified signature.

### 4.3 Data Validation

The application should require the following information:

| Field | Validation Requirement |
|---|---|
| Project Number | Mandatory; valid project identifier |
| Product | Selected from an approved component catalogue |
| Quantity | Positive numeric value |
| Employee | Identifies the requesting employee |
| Manager | Verified Microsoft 365 identity |
| Request Date | Automatically recorded |

The application should prevent submission when mandatory information is missing or invalid.

### 4.4 Product Catalogue

The proposed application would use a structured component catalogue.

Products could be organised into categories such as Mechanical, Electrical and Pneumatic.

Users could search by product category, description or component identifier.

This would simplify product selection and reduce inconsistent product descriptions.

The catalogue would require appropriate maintenance to ensure product information remains accurate.

### 4.5 Duplicate Request Handling

The Project Number must be provided before submitting a purchasing request.

The Purchasing Administrator would verify whether the same or similar products had already been requested or purchased for the specified project.

This verification should consider both pending purchasing requests and existing ERP purchasing records.

Potential duplicate requests should not automatically be rejected because repeated purchases can sometimes be legitimate.

The administrator would contact the manager for clarification where necessary.

### 4.6 Request Status Tracking

The initial status proposal included:

- Sent
- Purchased
- Received

Additional statuses may be introduced during implementation, including Pending Review, Rejected, Cancelled and Partially Received.

These additional statuses are recommendations for future development and have not yet been implemented.

### 4.7 Partial Delivery Handling

The system should record ordered quantities and received quantities.

For example:

| Component | Ordered | Received | Outstanding |
|---|---:|---:|---:|
| Sensor 24V | 20 | 12 | 8 |

The application could calculate outstanding quantities automatically.

A partially received order would remain open until the remaining components were received or the outstanding quantity was formally resolved.

The Purchasing Administrator or Stores personnel would remain responsible for following up with the supplier.

### 4.8 ERP Integration

Direct ERP integration cannot be assumed without confirming the available technical interfaces.

Possible approaches include:

- Manual transfer of purchasing information.
- CSV export from SharePoint and controlled import into the ERP system, if supported.
- Future automated integration through an approved API or compatible interface.

The proposed design retains manual Purchase Order creation as an initial control.

---

## 5. Conventional Automation vs AI

The proposed solution primarily relies on conventional automation.

Power Apps could support structured data entry, while SharePoint could store requests and product records.

Power Automate could manage notifications and workflow events.

AI is not currently required to implement these core features.

A possible future AI use case would involve identifying potentially duplicate requests when product descriptions differ.

However, this would require appropriate data access, reliable matching procedures and human review.

No AI functionality has been implemented or tested.

---

## 6. Results

The conceptual design established:

- A manager-controlled purchasing request process.
- Mandatory project identification.
- Structured product selection.
- Data validation requirements.
- Manual verification of potentially duplicate requests.
- Purchasing request status tracking.
- Partial delivery handling.
- Potential Microsoft Power Platform architecture.
- ERP integration options and limitations.

The design was reviewed through simulated business scenarios and discussion.

**No functional application, automated workflow or live integration was created during this laboratory.**

---

## 7. Limitations

The proposed solution remains conceptual.

The following areas require further investigation:

- Availability of appropriate Microsoft 365 and Power Platform licences.
- Authorisation and permission controls.
- Product catalogue maintenance.
- ERP import and integration capabilities.
- Data access and security.
- Application usability.
- Error handling and operational testing.

---

## 8. Lessons Learned

This laboratory demonstrated the importance of designing business workflows before implementing automation.

A simplified approval process can reduce unnecessary administrative work, but must maintain appropriate identity verification and accountability.

Structured data validation can prevent incomplete requests.

Duplicate detection requires business context rather than simply identifying repeated product codes.

Partial deliveries should be tracked using quantities as well as status information.

The exercise also reinforced the distinction between conventional automation and genuine AI-powered functionality.

---

## 9. Next Stage

**Lab 03 – Data Structure and Validation**

The next stage will focus on creating a small simulated product catalogue and purchasing request dataset.

The objective will be to develop and test essential validation rules using free tools before moving towards an application prototype.
