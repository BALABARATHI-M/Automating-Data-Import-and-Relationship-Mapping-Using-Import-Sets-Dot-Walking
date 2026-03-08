# Automating-Data-Import-and-Relationship-Mapping-Using-Import-Sets-Dot-Walking
**Platform:** ServiceNow PDI    
**Academic Year:** 2023-2026

---

## 👥 Team Members

| Member | Name |
|--------|------|
| Team Member 1 | BALABARATHI M |
| Team Member 2 | SILAMBARASAN A |
| Team Member 3 | HARIHARAN S |
| Team Member 4 | KISOTH M |

---

## 📌 Project Overview

This project automates the process of importing employee records from an external CSV/Excel file into ServiceNow and automatically mapping relationships between employees, departments, and managers using Dot Walking.

When an Incident is assigned to an employee, the Incident form automatically displays the employee's **Department**, **Email**, and **Manager** — without any manual lookup or custom scripting.

---

## 🎯 Objectives

- Import employee records (Name, Email, Department, Manager, Phone) from a CSV/Excel file using **Import Sets**
- Map staging table fields to the `sys_user` table using a **Transform Map**
- Auto-populate related employee fields on the Incident form using **Dot Walking**
- Achieve all objectives using 100% native ServiceNow configuration — no scripting required

---

## 🛠️ Technologies Used

| Technology | Purpose |
|------------|---------|
| ServiceNow PDI | Development and runtime environment |
| Import Sets | Bulk data import from external files |
| Transform Maps | Field mapping from staging to target table |
| Dot Walking | Auto-populate related fields on forms |
| Google Sheets | Employee data preparation |
| CSV / Excel | Data export format |

---

## 📁 Project Documents

| # | Document | Description |
|---|----------|-------------|
| 1 | `01_Ideation_Phase.pdf` | Problem discovery, brainstorming, and selected solution |
| 2 | `02_Requirement_Analysis.pdf` | Functional & non-functional requirements |
| 3 | `03_Project_Design_Phase.pdf` | System architecture, data model, and design decisions |
| 4 | `04_Project_Planning_Phase.pdf` | Timeline, milestones, WBS, and risk management |
| 5 | `05_Project_Development_Phase.pdf` | Step-by-step implementation guide with screenshot placeholders |
| 6 | `06_Project_Documentation.pdf` | Final project report with testing, challenges, and conclusion |

---

## 🎬 Project Demonstration Video

> Watch the full project walkthrough including data import, transform map configuration, and dot walking in action.

🔗 **[Click here to watch the Demo Video](https://drive.google.com/file/d/1C1FNa3cCnxCaM-4gHqu8s9FgOKACh6XB/view?usp=drive_link)**

---

## 🚀 How It Works

### Milestone 1 — Data Import
1. Employee data (4 records) is prepared in Google Sheets and exported as `.xlsx`
2. File is imported into ServiceNow via **System Import Sets → Load Data**
3. A staging table is created with all 5 fields
4. A **Transform Map** maps the staging fields to the `sys_user` table
5. **Mapping Assist** is used to manually map the Manager field
6. Transform is executed — all 4 records inserted with zero errors

### Milestone 2 — Dot Walking
1. Incident form layout is opened via **Context Menu → Configure → Form Layout**
2. Three dot-walked fields are added to the form:
   - `assigned_to.department` → Assigned to Department
   - `assigned_to.email` → Assigned to Email
   - `assigned_to.manager` → Assigned to Manager
3. When an Incident is assigned to an imported user, all three fields auto-populate instantly

---

## ✅ Results

| Test | Result |
|------|--------|
| 4 employee records imported into staging table | ✅ Pass |
| All 5 fields mapped correctly via Transform Map | ✅ Pass |
| 4 records inserted into sys_user with 0 errors | ✅ Pass |
| Dot-walked fields visible on Incident form | ✅ Pass |
| Department, Email, Manager auto-populate on Incident | ✅ Pass |

---

## 📚 References

- [ServiceNow Import Sets Documentation](https://docs.servicenow.com)
- [ServiceNow Dot Walking Documentation](https://docs.servicenow.com)
- [Naan Mudhalvan Program](https://naanmudhalvan.tn.gov.in)
