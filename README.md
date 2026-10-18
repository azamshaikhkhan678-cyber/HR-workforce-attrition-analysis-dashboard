# Enterprise HR Workforce Analytics & Attrition Console

## 🎯 Project Objective
This enterprise-grade Business Intelligence solution transforms raw transactional human resource records into a highly interactive operations dashboard. It enables executive teams, HR managers, and talent analysts to track workforce demographics, evaluate employee satisfaction, and monitor attrition rates to optimize corporate retention workflows.

## 📊 Dashboard Visual Architecture & Layout
The completed interface follows strict enterprise UI/UX standards, structured as follows:
* **Top KPI Layer:** High-level scoreboard cards tracking Total Headcount (10), Attrition Count (3), Attrition Rate % (30.0%), Average Job Satisfaction Score (3.50), and Average Monthly Income (₹73.10K).
* **Middle Analysis Section:** A Stacked Bar Chart mapping out exactly where attrition counts concentrate by department, alongside an interactive Donut Chart breaking down the total workforce gender distribution mix.
* **Bottom Granular Data Layer:** A comprehensive Matrix Table detailing individual employee parameters for deep-dive reporting.
* **Interactive Control Slicers:** Control checkboxes allowing users to dynamically filter the entire canvas layout by Department.

## 🧮 Custom HR Analytics Engineering (DAX Measures)
The following core calculations were engineered directly into the data engine to power the dashboard:
* **Total Employees:** `Total Employees = DISTINCTCOUNT(HR_Workforce_Data[EmployeeID])`
* **Attrition Volatility Count:** `Attrition Count = CALCULATE(COUNTROWS(HR_Workforce_Data), HR_Workforce_Data[Status] = "Left")`
* **Calculated Attrition Rate %:** `Attrition Rate % = DIVIDE([Attrition Count], [Total Employees], 0)`

## 📊 Technical Workspace File Deployment Notice
The dynamic visual charts, metrics, and slicers are fully compiled inside the main project workbook asset. Please download and open the `HR_Analytics_Dashboard.pbix` file using Microsoft Power BI Desktop to interactively test, filter, and view the live dashboard canvas.

## 📈 Strategic Corporate Insights Derived
* **Departmental Attrition Concentrations:** The data highlights that the Sales and Technology sectors show early volatility signals, requiring targeted talent retention adjustments.
* **Compensation Optimization Opportunities:** Employees experiencing standard salary compression beneath the organizational average demonstrate a higher trend line for voluntary departures.
