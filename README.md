# 🧠 Project 1 — Fake Attack Log Investigation (Splunk)

## 🎯 Objective
Simulate a security investigation using *Splunk Free (Local)* and public logs to detect suspicious login activities and understand how analysts use SIEM tools to identify potential threats.

---

## 🧩 Dataset
Downloaded from: [https://github.com/mdecrevoisier/EVTX-to-MITRE-Attack](https://github.com/mdecrevoisier/EVTX-to-MITRE-Attack)  
Type: Windows Event Logs (.evtx)

---

## ⚙️ Steps Summary
1. Installed and opened *Splunk Free* locally.  
2. Indexed .evtx files from the GitHub dataset.  
3. Used *Search & Reporting* to run basic queries:
   - Count all events:  
     
     index="evtx_mitre"
     
   - Failed login attempts:  
     
     index="evtx_mitre" EventCode=4625
     
   - Successful logins from unusual IPs:  
     
     index="evtx_mitre" EventCode=4624 NOT src_ip="192.168.*"
     
4. Created a *Dashboard* with:
   - Failed vs successful logins  
   - Top source IPs  
   - Timeline of login attempts  

---

## 📊 Dashboard Example
(Insert a screenshot here)  
Example:
![Dashboard Example](images/dashboard-example.png)

---

## 🔍 Results
- Detected multiple failed login attempts from external IPs.  
- Identified a successful login from a new country (possible credential compromise).  
- Visualized attack timeline and login patterns.

---

## 💡 Key Takeaways
- Learned how to index and query logs in Splunk.  
- Understood how Event IDs 4624 (login success) and 4625 (login failed) relate to authentication events.  
- Gained hands-on experience creating dashboards for attack detection.  

---

## 🚀 Next Steps
- Ingest Linux and network logs for correlation analysis.  
- Add alerts for unusual login times or IPs.  
- Simulate brute-force or phishing scenarios to expand the lab.

---

## 🧰 Tools Used
- *Splunk Free (Local)*  
- *Windows EVTX logs*  
- *Markdown for documentation (GitHub)*

---

## 👩‍💻 Author
Jessica Braz — Cybersecurity Student  
Location: Australia  
GitHub: https://github.com/jessicabraz

