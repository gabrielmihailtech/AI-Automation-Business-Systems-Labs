# Lab 01 – Business Process Analysis

**Project:** AI Automation & Business Systems  
**Lab Type:** Business Process Analysis  
**Environment:** Simulated Manufacturing Company  
**Status:** Completed – Analysis Only

---

## 1. Scenario

### Company Background

Westbridge Manufacturing Ltd. is a fictional Irish manufacturing company employing approximately 85 people.

The company uses an ERP system to manage purchasing, inventory and supplier records. However, its internal purchasing request process remains largely manual.

### Current Business Process

The existing purchasing workflow consists of the following steps:

1. An employee identifies the need for materials or components.
2. The employee sends a purchasing request by email.
3. The Purchasing Administrator reviews the request and records the information in Excel.
4. If information is missing, the administrator contacts the employee.
5. The request is forwarded to the department manager for approval.
6. After approval, the administrator manually creates a Purchase Order in the ERP system.

### Identified Business Problems

Management has reported several recurring issues:

- Purchasing requests frequently contain incomplete information.
- Employees and administrators exchange multiple emails to clarify requirements.
- Manager approvals are sometimes delayed or overlooked.
- Excel tracking records are not always updated.
- Employees have limited visibility of purchasing request statuses.
- Duplicate requests may occasionally be submitted.
- Management cannot easily monitor pending requests or processing times.

### Business Constraints

The company wants to improve its purchasing process without replacing the existing ERP system.

Microsoft 365, SharePoint and Power Automate are already available within the organisation.

Additional AI licences have not been approved.

The Purchasing Administrator must remain responsible for creating Purchase Orders, and purchasing requests require management approval.

---

## 2. Objective

Analyse the existing purchasing request process, identify inefficiencies and propose opportunities for process improvement and automation.

The analysis should determine whether conventional automation is sufficient or whether AI could provide additional business value.

---

## 3. Original Exercise Requirements

### Task 1 – Identify Process Problems

Identify at least three weaknesses in the current purchasing workflow.

Explain how these problems affect efficiency, communication or operational performance.

### Task 2 – Identify Automation Opportunities

Identify at least three activities that could potentially be automated.

Explain which activities would benefit from automation and why.

### Task 3 – Evaluate the Need for AI

Determine whether the proposed improvements require artificial intelligence or whether conventional automation technologies would be sufficient.

Justify the decision.

### Task 4 – Propose an Initial Solution

Describe a practical solution using suitable technologies, considering existing business systems, management approvals and ERP operations.

---

## 4. Business Process Analysis

### 4.1 Process Inefficiencies

The initial analysis identified that the purchasing request process involved unnecessary administrative steps and repeated communication between employees, managers and purchasing staff.

One significant issue was the submission of incomplete purchasing requests.

When a request did not contain the correct product information, quantities or project details, the Purchasing Administrator had to contact the employee to obtain clarification.

This created additional administrative work and delayed purchasing activities.

The existing workflow also involved several approval and communication stages that could potentially be simplified.

### 4.2 Opportunities for Process Improvement

A more efficient approach would involve employees reviewing their purchasing requirements directly with their department manager before submitting a request to Purchasing.

This would help ensure that product details and quantities are checked before the request enters the purchasing workflow.

A structured digital form could also reduce missing information by requiring employees or managers to select products from an existing component catalogue.

### 4.3 Proposed Technology

The following technologies were identified as potential components of a future solution:

| Technology | Potential Purpose |
|---|---|
| Microsoft Power Apps | Structured purchasing request interface |
| SharePoint Lists | Product catalogue and purchasing request records |
| Power Automate | Notifications and workflow automation |
| Microsoft 365 | User authentication and identity |
| ERP System | Purchase Order creation and purchasing history |
| Excel / CSV | Reporting and possible data exchange |

These technologies were considered during the initial analysis. No application or integration was implemented during this laboratory.

### 4.4 AI Assessment

The initial analysis concluded that artificial intelligence was not essential for the core purchasing request process.

Most identified problems involved incomplete information, manual communication, approval delays and inefficient data handling.

These problems could potentially be addressed through structured forms, validation rules and conventional workflow automation.

AI could be investigated in later development stages for more complex activities, such as identifying potentially duplicated requests when product descriptions differ.

However, this functionality would require reliable access to purchasing data and appropriate human verification.

---

## 5. Initial Proposed Solution

The proposed process would begin with an employee discussing purchasing requirements directly with the department manager.

A digital purchasing request system would then allow the manager to submit structured information to the Purchasing Administrator.

The application would use an organised component catalogue to simplify product selection and quantity entry.

Project identification would be mandatory.

The Purchasing Administrator would remain responsible for verifying purchasing information and creating Purchase Orders in the ERP system.

The objective is to reduce repeated communication and improve the quality of purchasing requests without replacing existing business systems.

---

## 6. Results

The laboratory produced the following outcomes:

- Identified inefficiencies in the existing purchasing request process.
- Recognised incomplete information and repeated communication as important operational problems.
- Proposed a structured digital purchasing request approach.
- Identified suitable Microsoft technologies for potential implementation.
- Distinguished conventional automation from AI-powered functionality.
- Established an initial direction for improving the purchasing process.

**No automation was built or tested during this laboratory.**

---

## 7. Limitations

This exercise was based on a fictional manufacturing company and a simulated purchasing scenario.

The analysis did not involve access to an actual ERP database, purchasing records or Microsoft Power Platform environment.

The proposed improvements have not yet been validated through implementation or user testing.

---

## 8. Lessons Learned

This laboratory demonstrated the importance of understanding an existing business process before developing an automation solution.

Introducing AI is not always necessary to improve business operations.

Simple workflow redesign, structured data collection and conventional automation may provide substantial improvements without additional technical complexity.

The analysis also highlighted the importance of considering existing business systems and the responsibilities of employees, managers and purchasing administrators.

---

## 9. Next Stage

**Lab 02 – Automation Solution Design**

The next laboratory will develop the initial proposal into a more detailed workflow design, including management approval, data validation, duplicate request handling, purchasing status tracking and partial deliveries.
