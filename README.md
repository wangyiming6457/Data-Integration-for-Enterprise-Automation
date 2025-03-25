# 📡 Telco Customer Notification Automation using Workato

## 📘 Project Overview

This project was developed as part of the **ANL555 - Data Integration for Enterprise Automation** course (January 2025 semester). Our team addressed a real-world enterprise challenge faced by a telco company: **delays and data privacy risks in notifying customers during network faults due to manual data handling**.

Our solution demonstrates a **secure, API-led, event-driven automation** that integrates CRM systems, detects service faults, and sends proactive notifications to affected customers—all while ensuring personally identifiable information (PII) is protected.

---

## 👨‍💻 Team Members

- **Wang Yiming (Leader)**   
- Li Jian   
- Teng Han Leng 
- Leow Yu Fan  

---

## 🎯 Objectives

- Secure real-time access to service data from **Juniper Networks**
- Integrate customer data from **Salesforce.com** (pre-paid) and **Amdocs** (post-paid)
- Automatically notify affected customers via **email/app**
- Store integrated data in **Snowflake** for analytics and predictive monitoring

---

## 🔐 Key Privacy & Data Handling Challenges

| Issue | Source | Safeguards |
|-------|--------|------------|
| Manual CSV extraction & Excel processing | Amdocs, Salesforce | ✅ API Integration, ✅ RBAC, ✅ Tokenization, ✅ TLS |
| Manual cross-referencing errors | Amdocs, Salesforce | ✅ Automated matching via Workato, ✅ SFTP, ✅ AES-256 Encryption |

📌 *Real-world breaches like Carousell’s and Singapore HSA's were studied as cautionary case studies.*

---

## 🧠 Proposed Solution Architecture

We adopted an **API-led integration with an event-driven microservice architecture**, built using:

- **Juniper Networks** (Network Faults)
- **API Gateway** (Secure CRM Access)
- **Workato** (Integration Platform as a Service - IPaaS)
- **Mistral AI** (Auto-generate messages)
- **Gmail** (Send notifications)
- **Snowflake** (Store logs for analytics)

### 🔄 Flow Summary:
1. **Juniper** sends a fault event →  
2. **Workato** triggers CRM queries →  
3. Customer list filtered/tokenized →  
4. AI-generated messages →  
5. Emails sent to affected users →  
6. Logs stored in **Snowflake**

---

## ⚙️ MVP Prototype

The MVP was implemented using **Workato**, simulating:
- Fault events (e.g., "Sentosa Outage")
- CRM record search and filtering
- AI-powered message generation (via Mistral AI)
- Real-time email alerts (via Gmail)
- Secure storage in Snowflake

### 📸 Screenshot (Insert architecture or flow image here if available)

---

## 📊 Results & Impact

| Metric | Manual | MVP | Improvement |
|--------|--------|-----|-------------|
| ⏱ Time to Notify | 30–60 mins | < 1 min | 95–98% faster |
| ✅ Accuracy | ~85–90% | >99% | Reduced human error |
| 📢 Proactive Rate | 0% | ~100% | Complete shift |
| 🔐 PII Risk | High | Low | Tokenization & Encryption |
| ⚙️ Scalability | Low | High | Real-time, reusable |

---

## 📈 Business Benefits

- **Customer Satisfaction**: Quicker, transparent service updates
- **Operational Efficiency**: No more CSV/Excel headaches
- **Data Compliance**: Stronger PII handling (RBAC, Tokenization, TLS)

---

## 📚 References

- Hamzah, A. (2024). *Carousell fined $58K for data breach*. [The Straits Times](https://www.straitstimes.com/singapore/carousell-fined-58k-for-data-breaches-including-one-where-data-of-26m-users-were-sold-on-hacking-forum)
- Kurohi, R. & Choo, F. (2019). *HSA data exposure incident*. [The Straits Times](https://www.straitstimes.com/singapore/health/personal-information-of-over-800000-blood-donors-exposed-online-hsa)

---

## 🚀 Future Enhancements

- Integration with **customer recovery vouchers**
- Support for **multi-channel messaging** (SMS, WhatsApp)
- Enhanced **dashboard analytics** via Snowflake

---

## 📂 Repository Structure

```bash
.
├── MVP_Architecture.png     # Architecture diagram (optional)
├── Workato_Recipe_Screenshot.png # MVP screenshot (optional)
├── README.md                # This file
└── ANL555_GBA_Report.docx   # Full report (optional for sharing)
