## 💼 Operations Analyst Portfolio Project: Cross-Timezone Resource Management

This project demonstrates proficiency in **data manipulation (Pandas), business analysis, and strategic communication** by simulating the day-to-day operational challenges of a global, mission-driven nonprofit. The goal was to transform raw data into **actionable operational insights** for management.

### 🛠️ Technical Workflow & Data Sources

The project utilized three synthetic, interconnected CSV files to model operational reality, showcasing the ability to join relational data:

| Data File | Purpose | Key Manipulation |
| :--- | :--- | :--- |
| `staff_roster.csv` | **Personnel:** Lists staff names, departments, and **ET/CET timezones**. | Merged with tasks using `Staff_ID`. |
| `project_tasks.csv` | **Core Schedule:** Defines effort (`FTE Days`), risk, and constraints. | **Filtered to only include active tasks** ('In Progress' and 'Blocked') to assess current burden. |
| `project_costs.csv` | **Financial Data:** Records external costs and vendor transactions. | Aggregated to analyze financial and administrative workload. |

## 🎯 Core Analytical Findings

The analysis was segmented to answer three core questions regarding **Active Workload** (In Progress/Blocked tasks only):

### 1. Resource Utilization & Overload Analysis

This analysis identifies staffing bottlenecks to prevent burnout and ensure timely delivery.

| Metric | Result | Strategic Insight |
| :--- | :--- | :--- |
| **Highest Overload** | **Trent Beard (115.01 Active FTE Days)** | Trent Beard, Melany Shaw, and Robert Floyd represent the highest active workload risk. |
| **Departmental Load** | Policy (**821** FTE Days) vs. Ops (**595** FTE Days) | Policy carries the highest strategic burden, but the Ops department is highly concentrated, with several employees near the top of the individual workload rankings. |

**Actionable Insight: Resource Redistribution**

To alleviate overload on the top staff while maintaining Policy project momentum, the analyst should propose specific task delegation:

* **Trent Beard (Policy):** Offload work to **Murphy Lin (56.48 FTE)** and **Martin Tran (66.45 FTE)**, who are lower-allocated staff within the Policy department.
* **Max Baxter (Comms):** Despite Comms having the lowest overall departmental load (**263** FTE), Max Baxter is heavily burdened (**104.72 FTE**). His work should be delegated to **April Quinn** or **Griffin Clarke** to preserve strategic communications capacity.

<table>
  <thead>
    <tr>
      <th scope="col">FTE Workload Days by Department</th>
      <th scope="col">FTE Workload Days by Employee</th>
    </tr>
    <body>
      <td>
        <img width="252" height="121" alt="image" src="https://github.com/user-attachments/assets/83f3eaff-931b-4de9-9e06-0d6a73f8f2f4" />
      </td>
      <td>
        <img width="341" height="550" alt="image" src="https://github.com/user-attachments/assets/cf5f88ea-a79a-4e9f-aadb-f1e5222f5807" />
      </td>
    </body>
  </thead>
</table>

### 2. Cross-Timezone Risk Prioritization

The **Operational Risk Index (ORI)**—calculated as Project Risk $\times$ Timezone Constraint—flags tasks most likely to fail due to complexity and cross-border scheduling friction.

| Department | Total ORI (Risk) | Insight |
| :--- | :--- | :--- |
| Policy | **1,975** | Highest risk concentration due to complexity and high dependencies. |
| Ops | **1,275** | Secondary risk, but critical for supporting the Policy team's highest-risk deliverables. |

**Actionable Insight: Targeted Risk Mitigation**

Melany Shaw's workload is concentrated with a critical **125 ORI** in the **EU AI Act Compliance** project. To reduce organizational risk without removing her from the critical team, the optimal strategy would be to delegate her specific, lower-priority tasks within that project to **Robert Floyd (35 ORI)** or **Mason Pace (19 ORI)**, who are already embedded in the project but carry a much lighter risk burden. This ensures high-risk projects are supported by staff with preserved capacity.

<table>
  <thead>
    <tr>
      <th scope="col">Risk by Department</th>
      <th scope="col">Risk by Project</th>
      <th scope="col">Heatmap: Project Risk by Employee</th>
    </tr>
    <body>
      <td>
        <img width="293" height="165" alt="image" src="https://github.com/user-attachments/assets/66a36451-77e5-4f6f-a954-98c7f2b0cf0c" />
      </td>
      <td>
        <img width="293" height="165" alt="image" src="https://github.com/user-attachments/assets/eaffaa00-48f8-49f7-b38c-7b906d0db1e1" />
      </td>
      <td>
        <img width="635" height="473" alt="image" src="https://github.com/user-attachments/assets/bdc73176-c631-4159-af45-e400330f93f6" />
      </td>
    </body>
  </thead>
</table>


### 3. Vendor Management & Financial Oversight

This analysis reveals both the **total financial spend** and the **administrative workload** required for vendor management (where Transactions = Administrative Load).

| Vendor/Tool | Total Spend (USD) | Average Spend (USD) | Transactions |
| :--- | :--- | :--- | :--- |
| **Coda.io** | $613,079 | $7,129 | **86** |
| **Legal Firm** | $528,322 | **$8,386** | 63 |

<table>
  <head>
    <tr>
      <th scope="col">Vendor Costs</th>
    </tr>
    <body>
      <td>
        <img width="700" height="301" alt="image" src="https://github.com/user-attachments/assets/47612745-6a74-4bc4-97cd-d903ee70c788" />
      </td>
    </body>
  </head>
</table>

**Actionable Insight:**
Actionable Insight: While Legal Fees have the highest average cost, **Coda.io** requires the highest number of transactions (86), signaling a large administrative workload for the Operations team. The optimal vendor strategy is to consolidate these licenses into a single annual contract to minimize administrative friction and save Ops time.

