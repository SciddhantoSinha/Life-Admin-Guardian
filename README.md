# 🛡️ Life Admin Guardian

> A multi-agent AI system built using Lyzr that analyzes personal administrative documents, identifies important deadlines, and provides practical next-step recommendations.



## 📌 Project Overview

Life Admin Guardian is a **multi-agent AI system** designed to help users understand and manage important information from personal administrative documents.

People often have documents such as invoices, receipts, warranty documents, bills, insurance documents, and purchase documents.

These documents may contain important information such as purchase dates, payment deadlines, warranty expiry dates, renewal dates, return deadlines, and important terms.

Life Admin Guardian uses a **Manager Agent and specialized AI sub-agents** to analyze this information and provide users with clear and practical guidance.



## 🎯 Problem Statement

Managing multiple personal documents can be difficult because important information is often spread across different documents.

For example, users may forget:

- When a bill needs to be paid
- When a product return period ends
- When a warranty expires
- When an insurance policy requires renewal
- Which documents contain important conditions or requirements

Life Admin Guardian helps organize this information and converts document details into useful actions.



## 💡 Solution

Life Admin Guardian uses a **multi-agent architecture**.

Instead of using one AI agent to perform every task, the system divides responsibilities among specialized agents.

The main Manager Agent understands the user's request and coordinates the appropriate specialized agents.

The system includes:

1. 🛡️ Life Admin Guardian — Manager Agent
2. 📄 Document Analyst
3. 📅 Deadline Tracker
4. ✅ Action Advisor



## 🏗️ Multi-Agent Architecture

```text
                    🛡️ LIFE ADMIN GUARDIAN
                         Manager Agent
                               │
                  Understands User Request
                               │
          ┌────────────────────┼────────────────────┐
          ↓                    ↓                    ↓
   📄 Document Analyst   📅 Deadline Tracker   ✅ Action Advisor
          │                    │                    │
          ↓                    ↓                    ↓
 Extract information      Identify important      Recommend
 from documents          dates and deadlines     next actions
          │                    │                    │
          └────────────────────┼────────────────────┘
                               ↓
                    Manager combines results
                               ↓
                       Final response to user

```

## 🤖 Agents

### 🛡️ 1. Life Admin Guardian — Manager Agent

The Manager Agent is the central coordinator of the system.

#### Responsibilities

- Understand the user's request
- Determine which specialized agents are required
- Delegate tasks to the appropriate agents
- Coordinate multiple agents when necessary
- Combine the results into one structured response

#### Example Workflow

Document Analyst  
↓  
Deadline Tracker  
↓  
Action Advisor  
↓  
Final Response



### 📄 2. Document Analyst

The Document Analyst extracts important information from personal administrative documents.

#### Supported Document Types

- Invoices
- Receipts
- Warranty documents
- Bills
- Insurance documents
- Purchase documents

#### Information Extracted

When available, the agent identifies:

- Product or service name
- Purchase date
- Purchase price
- Warranty period
- Warranty expiry date
- Return period
- Return deadline
- Payment due date
- Renewal date
- Expiry date
- Important terms
- Required actions

#### Important Rule

The agent only extracts information that is actually available in the document.

If information cannot be found, it clearly states that it is unavailable.



### 📅 3. Deadline Tracker

The Deadline Tracker identifies and organizes important dates and deadlines.

#### It focuses on:

- Return deadlines
- Warranty expiry dates
- Bill payment due dates
- Insurance renewal dates
- Subscription renewal dates
- Document expiry dates
- Service dates
- Maintenance dates

For every important date, the agent identifies:

1. What the date relates to
2. The actual date
3. Why the date is important
4. Whether the user may need to take action



### ✅ 4. Action Advisor

The Action Advisor converts document information and deadlines into practical recommendations.

The agent can help when:

- A product return deadline is approaching
- A warranty is nearing expiry
- A bill needs to be paid
- An insurance policy requires renewal
- A maintenance date is approaching

For every recommendation, the Action Advisor:

1. Explains what needs attention
2. Explains why it matters
3. Provides practical next steps
4. Helps prioritize important actions

The agent does not claim that an action has already been completed.



## 🔄 System Workflow

User Uploads Document  
↓  
Life Admin Guardian  
↓  
Manager understands request  
↓  
Document Analyst  
↓  
Extracts document information  
↓  
Deadline Tracker  
↓  
Identifies important dates  
↓  
Action Advisor  
↓  
Provides practical recommendations  
↓  
Manager combines results  
↓  
Final structured response

The Manager Agent may use only the agents required for a particular request.

### Document Extraction Request

User  
↓  
Manager  
↓  
Document Analyst  
↓  
Final Response

### Document + Deadline Request

User  
↓  
Manager  
↓  
Document Analyst  
↓  
Deadline Tracker  
↓  
Final Response

### Complete Analysis Request

User  
↓  
Manager  
↓  
Document Analyst  
↓  
Deadline Tracker  
↓  
Action Advisor  
↓  
Final Response



## 🧪 Testing

The system was tested using multiple types of sample documents.

### 💻 Laptop Invoice

**Test Prompt:**

> Analyze this document, identify all important deadlines, and tell me what actions I should take.

The system identified:

- Product information
- Purchase date
- Purchase price
- Warranty period
- Warranty expiry date
- Return period
- Return deadline
- Important terms
- Recommended actions



### 📶 Internet Bill

**Test Prompt:**

> Analyze this internet bill, identify the payment amount and payment due date, explain any important terms, and tell me what actions I should take before the deadline.

The system identified:

- Service provider
- Billing information
- Payment amount
- Payment due date
- Payment status
- Late payment information
- Required actions



### 🧺 Washing Machine Warranty

**Test Prompt:**

> Analyze this warranty document, identify the product details, warranty period and expiry date, explain the warranty coverage and important terms, and tell me what actions I should take.

The system identified:

- Product information
- Purchase date
- Warranty period
- Warranty expiry date
- Warranty coverage
- Exclusions
- Required documents for warranty claims
- Recommended actions



### 🏥 Health Insurance Policy

**Test Prompt:**

> Analyze this insurance policy, identify the policy expiry date and renewal date, explain the important policy information, and tell me what actions I should take before renewal. Clearly distinguish information extracted from the document from general recommendations.

The system identified:

- Policy information
- Policy expiry date
- Renewal date
- Renewal premium
- Important policy terms
- Actions required before renewal



## 📊 Example Output

### Important Dates and Deadlines

- **Purchase Date:** August 10, 2026
- **Return Deadline:** August 24, 2026
- **Warranty Expiry Date:** August 10, 2028

### Extracted Information

- **Product:** NovaBook Pro 15 Laptop
- **Warranty Period:** 2 years
- **Return Period:** 14 days

### Recommended Actions

- Keep the original invoice safe
- Keep the original product packaging
- Check the product before the return deadline
- Contact customer support if an eligible manufacturing defect occurs
- Retain warranty documents until the warranty expires



## 🛠️ Technologies Used

- Lyzr Agent Studio
- Large Language Models
- Multi-Agent Architecture
- Manager Agent
- Specialized AI Agents
- Document Analysis



## ⭐ Key Features

- Multi-agent AI architecture
- Manager-based agent orchestration
- Document information extraction
- Deadline identification
- Warranty tracking
- Payment due-date tracking
- Policy renewal tracking
- Practical action recommendations
- Structured responses
- Multiple document type support



## 🔐 Privacy and Data Handling

Life Admin Guardian is designed to analyze user-provided information.

The system is designed to:

- Avoid inventing information
- Clearly identify unavailable information
- Distinguish extracted document facts from AI-generated recommendations
- Avoid unnecessary exposure of sensitive personal information

For demonstrations and testing, synthetic sample documents should be used instead of real personal documents.



## 📁 Repository Structure

Life-Admin-Guardian/

├── README.md  
│  
├── screenshots/  
│   ├── manager-agent.png  
│   ├── document-analyst.png  
│   ├── deadline-tracker.png  
│   ├── action-advisor.png  
│   └── testing-results.png  
│  
└── sample-documents/  
    ├── sample_laptop_invoice.pdf  
    ├── sample_internet_bill.pdf  
    ├── sample_washing_machine_warranty.pdf  
    └── sample_health_insurance_policy.pdf



## 📸 Screenshots

### Manager Agent

![Life Admin Guardian Manager](screenshots/manager-agent.png)

### Document Analyst

![Document Analyst](screenshots/document-analyst.png)

### Deadline Tracker

![Deadline Tracker](screenshots/deadline-tracker.png)

### Action Advisor

![Action Advisor](screenshots/action-advisor.png)

### Testing Results

![Testing Results](screenshots/testing-results.png)



## 🚀 Future Improvements

Possible future enhancements include:

- Automatic document categorization
- Calendar integration for deadline reminders
- Email notifications
- Automated warranty tracking
- Automated bill reminders
- Document history
- Priority-based notifications
- More specialized AI agents
- Integration with personal productivity tools



## 🌟 Why Multi-Agent Architecture?

A single AI agent can perform multiple tasks, but Life Admin Guardian divides responsibilities among specialized agents.

Single Agent  
↓  
One agent performs every task

Compared with:

Multi-Agent System  
↓  
Manager Agent  
↓  
Specialized Agents  
↓  
Coordinated Results

This architecture allows each specialized agent to focus on a specific responsibility.

The Manager Agent determines which agents should be used depending on the user's request.



## 💬 Example Use Cases

### Use Case 1 — Laptop Purchase

A user uploads a laptop invoice and asks:

> What information is important, and what should I do?

The system can:

- Extract purchase information
- Identify the return deadline
- Identify warranty expiry
- Recommend actions

### Use Case 2 — Internet Bill

A user uploads an internet bill.

The system can:

- Identify the payment amount
- Find the due date
- Explain late-payment consequences
- Recommend paying before the deadline

### Use Case 3 — Warranty Document

A user uploads a product warranty.

The system can:

- Identify the product
- Find the warranty period
- Identify the warranty expiry date
- Explain coverage and exclusions

### Use Case 4 — Insurance Policy

A user uploads an insurance policy.

The system can:

- Identify policy dates
- Find the expiry date
- Identify the renewal date
- Explain important terms
- Recommend preparation before renewal



## 👨‍💻 Project Type

**Multi-Agent AI System**

**Domain:** AI Agents / Agentic AI / Personal Administration

**Architecture:**

Manager Agent  
+  
Specialized AI Agents  
↓  
Multi-Agent Orchestration



## 🏁 Conclusion

Life Admin Guardian demonstrates how a **Manager Agent can coordinate multiple specialized AI agents** to solve a real-world personal administration problem.

The system:

1. Extracts information from documents
2. Identifies important deadlines
3. Provides practical recommendations
4. Produces a structured final response

This project demonstrates practical implementation of:

- AI Agents
- Multi-Agent Systems
- Agent Orchestration
- Document Analysis
- Agent Specialization
- AI-powered decision support



## 👤 Author

**Sciddhanto Sinha**
