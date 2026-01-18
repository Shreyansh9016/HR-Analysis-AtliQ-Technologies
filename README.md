<h1>AtliQ HR Presence Dashboard</h1>

<h2>📌 Project Overview</h2>
<p>
This project focuses on analyzing employee attendance and work patterns for <strong>AtliQ Technologies</strong> using 
<strong>Excel, Power Query, DAX, and Power BI</strong>.
The dashboard enables HR teams to monitor presence, work-from-home (WFH) trends, sick leave (SL), and overall attendance behavior.
</p>

<p>
The source attendance data was maintained in a <strong>cross-tab (date-wise column)</strong> format for multiple months 
(April–June 2022). To ensure consistency, scalability, and analytical readiness, the data was transformed into a normalized structure using Power Query.
</p>

<hr>

<h2>🧩 Problem Statement</h2>
<ul>
  <li>Understand <strong>working preferences</strong> of employees (WFH vs WFO)</li>
  <li>Measure <strong>overall presence percentage</strong></li>
  <li>Analyze whether WFH is preferred at the <strong>beginning or end of the week</strong></li>
  <li>Track <strong>sick leave (SL) percentage</strong></li>
</ul>

<p><strong>Challenges:</strong></p>
<ul>
  <li>Month-wise data stored one below another (April, May, June)</li>
  <li>Dates present as columns causing schema inconsistency</li>
  <li>Not directly usable for Power BI analysis</li>
</ul>

<hr>

<h2>🛠 Tools & Technologies</h2>
<ul>
  <li>Microsoft Excel – Raw attendance data</li>
  <li>Power Query – Data cleaning & transformation</li>
  <li>Power BI – Data modeling and dashboarding</li>
  <li>DAX – KPI and percentage calculations</li>
</ul>

<hr>

<h2>📊 Dataset Details</h2>
<p><strong>Organization:</strong> AtliQ Technologies</p>
<p><strong>Date Range:</strong> April 2022 – 16 June 2022</p>
<p><strong>Granularity:</strong> Employee × Date</p>

<h3>Attendance Codes</h3>
<table border="1" cellpadding="6" cellspacing="0">
  <tr><th>Code</th><th>Meaning</th></tr>
  <tr><td>P</td><td>Present</td></tr>
  <tr><td>WO</td><td>Weekly Off</td></tr>
  <tr><td>WFH</td><td>Work From Home</td></tr>
  <tr><td>SL</td><td>Sick Leave</td></tr>
  <tr><td>PL</td><td>Paid Leave</td></tr>
  <tr><td>Others</td><td>Maintained as per source Excel</td></tr>
</table>

<hr>

<h2>🔄 Data Transformation (Power Query)</h2>

<h3>1️⃣ Template-Based Design</h3>
<p>
A reusable transformation template was created for one month and applied consistently across April, May, and June.
</p>

<h3>2️⃣ Unpivoting Date Columns</h3>
<ul>
  <li>Selected Employee Code and Employee Name</li>
  <li>Used <strong>Unpivot Other Columns</strong></li>
  <li>Converted date headers into row values</li>
</ul>

<h3>3️⃣ Worksheet Parameter</h3>
<ul>
  <li>Created a parameter named <strong>Worksheet</strong></li>
  <li>Filtered rows dynamically where Sheet Name = Worksheet</li>
  <li>Enabled reuse of logic for all months</li>
</ul>

<h3>4️⃣ Custom Function</h3>
<p>
A Power Query function was built to accept worksheet names as input and return standardized attendance data using the template logic.
</p>

<h3>5️⃣ Date Type Issue & Fix</h3>
<ul>
  <li>Initial issue: May & June data searched for April dates</li>
  <li>Cause: Early date-type conversion</li>
  <li>Fix: Removed premature date conversion step</li>
</ul>

<h3>6️⃣ Derived Columns</h3>
<ul>
  <li>Month (Apr 22, May 22, Jun 22)</li>
  <li>Day of Week</li>
  <li>WFH Count</li>
  <li>SL Count</li>
</ul>

<hr>

<h2>📐 Data Model</h2>
<p>
Star-schema inspired model optimized for performance and DAX calculations.
</p>

<hr>

<h2>📈 KPIs & Metrics</h2>
<ul>
  <li>Presence %</li>
  <li>WFH %</li>
  <li>Sick Leave %</li>
  <li>Day-wise Presence Trend</li>
  <li>Employee-wise Presence, WFH, and SL %</li>
</ul>

<hr>

<h2>📊 Dashboard Features</h2>
<ul>
  <li>Main HR Presence Dashboard</li>
  <li>Month-wise Dashboards (April, May, June)</li>
  <li>Focus Mode views for Presence %, WFH %, SL %</li>
  <li>Detailed employee-level tables</li>
</ul>

<hr>

<h2>🎛 Filters & Slicers</h2>
<ul>
  <li>Date</li>
  <li>Employee Name</li>
  <li>Day of Week</li>
</ul>

<hr>

<h2>🎯 Target Audience</h2>
<ul>
  <li>Beginners learning Excel & Power Query</li>
  <li>Corporate HR analytics teams</li>
</ul>

<hr>

<h2>📸 Dashboard Snapshots</h2>

<p><strong>Main Dashboard</strong></p>
<img src="https://github.com/user-attachments/assets/1f28d210-74be-4b12-80b5-f54f3e6b208f" />

<p><strong>Monthly Dashboards</strong></p>
<img src="https://github.com/user-attachments/assets/900a1beb-ced8-4cc4-b76e-b59a42229452" />
<img src="https://github.com/user-attachments/assets/53a71c30-70a2-476d-b172-0eea20958345" />
<img src="https://github.com/user-attachments/assets/1d40e1b2-b6cf-4cf9-acc8-4192147f2bef" />

<p><strong>Focus Mode Analysis</strong></p>
<img src="https://github.com/user-attachments/assets/f3455e72-ce82-482e-8e54-cdebcd2a8438" />
<img src="https://github.com/user-attachments/assets/c7d2198b-82ac-4b3f-b798-c68230be04f5" />
<img src="https://github.com/user-attachments/assets/7f0e14fc-bb50-42ae-9d84-73d644836978" />

<p><strong>Employee-Level Tables</strong></p>
<img src="https://github.com/user-attachments/assets/cfed222e-178a-4113-a442-1193efc709d0" />
<img src="https://github.com/user-attachments/assets/869ca143-7ddc-4bce-966c-092aa3bafba7" />

<hr>

<h2>🚀 Key Learnings</h2>
<ul>
  <li>Handling inconsistent Excel schemas</li>
  <li>Reusable Power Query transformations</li>
  <li>Importance of correct data type sequencing</li>
  <li>Converting raw attendance logs into HR insights</li>
</ul>

<hr>

<h2>👤 Author</h2>
<p>
<strong>Shreyansh Singh</strong><br>
Data Analyst
</p>

<hr>

<h2>📎 How to Use</h2>
<ol>
  <li>Clone or download the repository</li>
  <li>Open the Power BI file</li>
  <li>Use slicers to explore insights</li>
</ol>

<p>⭐ If you found this project useful, consider starring the repository.</p>
