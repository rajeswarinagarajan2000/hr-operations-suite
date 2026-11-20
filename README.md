# HR Operations Suite

A connected HR and finance back office built on the Microsoft Power Platform, using **one Dataverse data model** instead of separate demos.

> Portfolio project by **Rajeswari Nagarajan** · Built Nov 2026 · All data is fictional sample data.

**Live demo and screenshots:** [Portfolio → HR Operations Suite](https://rajeswarinagarajan2000.github.io/#p-hr)
**Live Power BI dashboard:** [Open HR dashboard](https://app.powerbi.com/view?r=eyJrIjoiMWE5MDgwYWYtNzI1My00MjNlLTljMzUtNjdhYjk2ZjQ5YmI4IiwidCI6ImRjMzgyZTVkLTUwZjUtNDQ5Ny1hN2U2LTAxY2QzMGUxNTkyNSJ9)

## What it does

| Part | Tools | Summary |
|---|---|---|
| Employee Management | Power Apps (model-driven), Dataverse | HR Operations Hub app on 8 related tables, business rules, custom security role |
| Automated Onboarding | Power Automate | 3 flows: create each new hire's task checklist from templates, update onboarding status, email overdue-task alerts |
| HR Performance Dashboard | Power BI, DAX | Headcount, attrition %, new hires, onboarding progress, overdue tasks |
| AI Invoice Processing | Power Automate, AI Builder, Approvals | Reads PDF invoices from OneDrive, matches or creates the vendor, saves the invoice, sends low-confidence (<80%) or high-value (>₹50,000) invoices for approval |
| Employee Help Agent | Copilot Studio | *In progress* |

## Dataverse tables

Employee · Department · Job Role · Location · Onboarding Template · Onboarding Task · Vendor · Invoice (publisher prefix `rjn_`)

## Power Automate flows

1. **Onboarding – Create Tasks:** new hire added → checklist built from templates → email sent
2. **Onboarding – Mark Complete:** task updated → open tasks checked → onboarding status updated
3. **Onboarding – Overdue Reminder:** scheduled → overdue tasks → HTML table email
4. **Invoice – Process with AI:** AI Builder → vendor lookup → invoice saved → approval if needed

## Files

- `HROperationsSuite_1_0_0_4.zip`: unmanaged solution export (tables, app, security role, flows, connection references)

## How to import

1. Go to [make.powerapps.com](https://make.powerapps.com) and pick a Developer environment.
2. **Solutions → Import solution** → choose the zip.
3. Create or select connections when asked: Dataverse, OneDrive for Business, Office 365 Outlook, Approvals.
4. Turn on the 4 flows. AI Builder "Process invoices" needs AI Builder credits.

## Contact

[LinkedIn](https://www.linkedin.com/in/rajeswari-nagarajan-4632503a1/) · [Portfolio](https://rajeswarinagarajan2000.github.io/)
