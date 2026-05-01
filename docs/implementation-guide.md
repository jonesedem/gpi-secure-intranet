# Implementation Guide: GPI Secure Intranet

## Overview
This document outlines the step-by-step implementation of a low-cost, secure intranet infrastructure using open-source tools and repurposed hardware.

---

## Phase 1: Planning & Requirements

### Objectives:
- Secure internal communication
- Centralized storage and backup
- Reduce dependency on internet
- Digitize internal processes

### Key Considerations:
- Budget constraints
- Available hardware (old desktops)
- Staff technical capacity
- Future scalability

---

## 🔌 Phase 2: Network Setup

### Steps:
1. Set up physical network (Ethernet cabling)
2. Install PoE switch
3. Configure IP addressing scheme
4. Connect all endpoints (servers + user systems)

---

## Phase 3: Firewall Configuration (pfSense)

### Installation:
- Installed pfSense on repurposed desktop

### Configured:
- NAT (internet access control)
- DHCP server
- DNS forwarding
- Firewall rules (allow/deny traffic)
- Basic VPN setup (optional)

---

## Phase 4: Server Deployment

### Application Server:
- Installed SME Server / NethServer
- Configured:
  - Internal email
  - HR system
  - ERP components
  - eLearning platform

### Domain Services:
- User authentication
- Role-based access

---

## Phase 5: Storage Setup (NAS)

### Installed:
- FreeNAS (TrueNAS CORE)

### Configured:
- ZFS file system
- RAID/mirroring for redundancy
- Shared folders
- Access permissions

---

## Phase 6: Internal Cloud & File Sharing

- Created shared directories
- Configured user access levels
- Enabled file upload/download within LAN

---

## Phase 7: Internal Communication

- Configured internal email system
- Enabled communication without internet

---

## Phase 8: User Setup & Training

- Created user accounts
- Assigned permissions
- Conducted staff training sessions
- Provided usage documentation

---

## Phase 9: Backup & Redundancy

- Configured scheduled backups
- Enabled storage redundancy (RAID)

---

## Deployment Outcome

- Fully functional intranet
- Secure file storage system
- Digitized HR and internal processes
- Reduced IT costs significantly

---

## Future Improvements

- Cloud integration (Azure/AWS)
- VPN for remote access
- SIEM monitoring