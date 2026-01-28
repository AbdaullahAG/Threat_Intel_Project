# Threat_Intel_Project
A Python-based SOAR tool designed to automate the extraction, filtration, and reputation checking of IP addresses from log files. It integrates with **AbuseIPDB API** to enrich indicators of compromise (IOCs) and generates comprehensive Excel reports for SOC analysts.

## 🚀 Features
- **Automated Extraction:** Uses Regex to identify IPv4 addresses from raw text/logs.
- **Smart Filtration:** Automatically filters out private (RFC 1918), loopback, and multicast IPs to save API quota.
- **Threat Enrichment:** Queries AbuseIPDB API for geolocation, ISP, usage type, and abuse confidence scores.
- **Rate Limit Handling:** Implements sleep mechanisms to respect API limits.
- **Reporting:** Exports clean, structured data to Excel (`.xlsx`) for immediate analysis.

## 🛠️ Tech Stack
- **Python 3.x**
- **Libraries:** `Pandas`, `Requests`, `Regular Expressions (re)`, `ipaddress`
- **API:** AbuseIPDB

## 📂 Project Structure
1. **Extraction:** Parsing unstructured log data.
2. **Validation:** distinguishing between Public vs. Private IPs.
3. **Enrichment:** Fetching threat intelligence data.
4. **Reporting:** Data visualization in Excel.

## ⚙️ How to Run
1. Clone the repository.
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
Open the Jupyter Notebook (.ipynb).

Insert your AbuseIPDB API Key in the configuration cell.

Run the cells to process your logs.

📊 Output Example
The tool generates a report containing:

IP Address

Abuse Confidence Score (0-100%)

ISP & Domain

Country of Origin

⚠️ Disclaimer
This tool is for educational and defensive purposes only. Ensure you have the appropriate permissions before analyzing log files.
