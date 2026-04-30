# Security Design: GPI Intranet Infrastructure

## 📌 Overview
Security was a core consideration in the design and implementation of the GPI intranet system, ensuring data confidentiality, integrity, and availability.

---

## 🧱 Security Architecture

The system was designed using a layered approach:

1. Perimeter Security (Firewall)
2. Internal Network Controls
3. Application-Level Security
4. Data Protection & Backup

---

## 🔐 Perimeter Security

### pfSense Firewall:
- Network traffic filtering
- NAT control
- Port management
- VPN capability (optional)

### Controls Implemented:
- Restricted inbound traffic
- Controlled outbound traffic
- Segmentation between external and internal network

---

## 🌐 Network Security

- Private IP addressing (LAN)
- Controlled access via switch
- Separation of user devices and servers

---

## 👥 Access Control

- User authentication via domain server
- Role-based access to systems
- Permissions for file sharing

---

## 💾 Data Security

- Centralized storage (NAS)
- RAID/mirroring for redundancy
- Controlled file access

---

## 🔄 Backup & Recovery

- Regular backup configuration
- Redundant storage using ZFS
- Recovery readiness for system failure

---

## 📧 Communication Security

- Internal email system (isolated from internet)
- Reduced exposure to external threats

---

## ⚠️ Risks Identified

- Limited physical security controls
- No advanced SIEM monitoring at the time
- Dependency on local infrastructure

---

## 🔧 Recommended Improvements (Modern)

- Implement Zero Trust Architecture
- Deploy SIEM (Azure Sentinel / Splunk)
- Enable Multi-Factor Authentication (MFA)
- Encrypt sensitive data at rest and in transit
- Use secure cloud backup

---

## 🎯 Security Outcome

- Reduced exposure to external threats
- Improved data protection
- Controlled internal access