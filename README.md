# Cloud-Cover: Azure Brute Automated Reporting Pipeline

-Cloud-Cover is a prototype security automation solution built in Azure.  
-It identifies (for example) brute force login attempts, extracts the top attacking IPs, and generates reports for further analysis.
-But logic app is setup to be flexible and adjust as you see fit (can easily change KQL code).

---

## ✅ **Current Features**
- Runs a KQL query in Microsoft Sentinel / Log Analytics Workspace (LAW) to identify brute force attacks (Event ID 4625).
- Summarizes and extracts top N attacker IPs from a defined time window (e.g. 24 or 48 hours).
- Logic App automatically exports the data as a CSV and emails it (e.g. to Outlook).
- Python scripts generate bar charts from the CSV showing the top attacker IPs (as shown below).

---

## 📊 **Example Output**

![Top 20 IPs](insert_screenshot_link_or_relative_path.png)

*Bar chart of top 20 IPs by failed login count — generated from Logic App CSV export.*

---

## 🌟 **Planned Enhancements**
- Fully automate graph generation (bar chart, heatmap, etc.) as part of the Logic App / Azure pipeline.
- Remove manual CSV download and Bash file-moving steps.
- Automatically email visualizations directly to Outlook as an attachment.
- (Optional) Enrich IPs with GeoIP location or reputation scoring.

---

## 🛠 **Architecture (Phase 1)**

# Cloud-Cover.2
Automated Version of Original Cloud-Cover
