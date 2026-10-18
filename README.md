# Enterprise HR Workforce Analytics & Attrition Console

## 🎯 Project Objective
This enterprise-grade Business Intelligence solution transforms raw transactional human resource records into an interactive operations dashboard. It enables executive teams, HR managers, and talent analysts to track workforce demographics, evaluate employee satisfaction scores, and monitor attrition rates to optimize corporate retention workflows.

## 📊 Dashboard Visual Architecture & Layout
The completed interface follows strict enterprise UI/UX standards, structured as follows:
* **Top KPI Scoreboard Layer:** Displays high-level cards tracking Total Headcount (10), Attrition Count (3), Attrition Rate % (30.0%), Average Job Satisfaction Score (3.50), and Average Monthly Income (₹73.10K).
* **Middle Analysis Section:** A Stacked Bar Chart mapping out attrition counts by department, alongside an interactive Donut Chart breaking down the total workforce gender distribution mix.
* **Bottom Granular Data Layer:** A comprehensive Matrix Table detailing individual employee parameters for deep-dive reporting.
* **Interactive Control Slicers:** Control checkboxes allowing users to dynamically filter the entire canvas layout by Department.

## ## 📸 Completed Interactive Interface Preview
## 📸 Completed Interactive Interface Preview
Please download and review the uploaded `HR_Analytics_Dashboard.pbix` workspace file inside this repository to interactively click, filter, and audit the live human resource analytics visuals.

 Custom HR Analytics Engineering (DAX Measures)
The following core calculations were engineered directly into the data engine to power the dashboard:
* **Total Employees:** `Total Employees = DISTINCTCOUNT(HR_Workforce_Data[EmployeeID])`
* **Attrition Volatility Count:** `Attrition Count = CALCULATE(COUNTROWS(HR_Workforce_Data), HR_Workforce_Data[Status] = "Left")`
* **Calculated Attrition Rate %:** `Attrition Rate % = DIVIDE([Attrition Count], [Total Employees], 0)`

## 📸 Completed Interactive Interface Preview
<p align="center">
  <img src="1.png" alt="HR Analytics Dashboard Interface" width="95%">
</p>

## 📈 Strategic Corporate Insights Derived
* **Departmental Attrition Concentrations:** The data highlights that the Sales and Technology sectors show early volatility signals, requiring targeted talent retention adjustments.
* **Compensation Optimization Opportunities:** Employees experiencing standard salary compression beneath the organizational average demonstrate a higher trend line for voluntary departures.
