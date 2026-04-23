# 🔐 Linux Log Analysis & SSH Attack Detection using Splunk

## 📌 Project Overview

This project demonstrates how to build a **home SOC (Security Operations Center) lab using Splunk** to monitor Linux authentication logs and detect real-world attack scenarios.

The objective is to simulate attacker behavior and perform **log-based detection using SPL (Splunk Processing Language)**.

---

## 🧱 Architecture
``` text
Kali Linux (Log Source)
         ↓
Splunk Universal Forwarder
         ↓
Splunk Enterprise (Windows)
         ↓
Detection & Visualization
```

---

## 🎯 Objectives

- Collect and forward Linux logs to Splunk  
- Analyze authentication logs (`auth.log`)  
- Detect SSH brute force attacks  
- Identify successful login after multiple failures  
- Monitor privilege escalation activity  
- Build detection queries and dashboards  

---

## ⚙️ Lab Setup

### 🔹 Splunk Enterprise (Windows)
- Installed and configured Splunk Web (`localhost:8000`)
- Enabled data receiving on port **9997**

### 🔹 Splunk Universal Forwarder (Kali Linux)
- Installed forwarder on Kali Linux
- Connected to Splunk server
- Configured log monitoring:

```bash
/var/log/auth.log
```


---

## 🧪 Attack Simulation

The following activities were performed to generate logs:

### 🔹 Multiple failed SSH login attempts

<img src="screenshots/fail.png" width="800"/>


<img src="screenshots/failed-attempts.png" width="800"/>

### 🔹 Successful SSH login

<img src="screenshots/accepted-password.png" width="800"/>


### 🔹 Privilege escalation using sudo

<img src="screenshots/splunk-sudo.png" width="800"/>


### 🔹 User activity simulation

<img src="screenshots/timechart.png" width="800"/>


## 📊 Dashboard

The Splunk dashboard includes:

- Failed login attempts over time
- Top attacker IP addresses
- Successful vs failed login activity
- Privilege escalation monitoring

💡 Key Learnings
- Hands-on experience with Splunk SIEM
- Understanding Linux authentication logs
- Writing detection logic using SPL
- Identifying attack patterns from raw logs
- Troubleshooting log ingestion issues
- Building real-world SOC detection workflows

## 🚨 Challenges & Solutions

| Issue                       | Resolution                               |
| --------------------------- | ---------------------------------------- |
| Forwarder not connecting    | Enabled port 9997 + firewall rules       |
| No logs visible             | Fixed monitor configuration & time range |
| `auth.log` not updating     | Enabled logging service                  |
| SSH connection refused      | Started SSH service                      |
| Detection query not working | Adjusted threshold logic                 |

## 🚀 Future Enhancements
- Integrate Wazuh for advanced detection
- Implement MITRE ATT&CK mapping
- Create automated alerts
- Add advanced correlation rules

## 🔥 Conclusion

This project demonstrates a practical SOC workflow:

log collection → analysis → detection → visualization.

It provides hands-on experience in SIEM operations and threat detection, aligned with real-world SOC analyst responsibilities.

## 📸 Screenshots

All screenshots are available in the `screenshots/` folder.

---

## 🔗 Connect With Me

- 🌐 Portfolio: https://www.cybergodfather.me  
- 💼 LinkedIn: https://linkedin.com/in/manoj-root  
- 🐙 GitHub: https://github.com/Manoj-Root  

---

## ⭐ Support

If you found this project useful, consider giving it a ⭐
