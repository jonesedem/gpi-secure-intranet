# Implementation Guide: Low-Cost Intranet for Nigerian Non-Profits (Updated 2026)

This guide provides both the **original 2017/2018 setup** I implemented at Girls’ Power Initiative Calabar and **modern recommendations** using current open-source tools that are easier to maintain.

### Original 2017/2018 Architecture (What I Built)

- **Firewall/Router**: pfSense on recycled PC
- **Main Server**: SME Server (Kozali) / NethServer
- **Storage**: FreeNAS with ZFS RAID
- **Network**: POE Switch
- **Applications**: Custom HR system, Internal email, Cloud file storage, Library system

**Key Achievement**: Delivered far beyond the original objectives while saving over ₦1.3 million.

### Modern Recommended Stack (2026) – Easier & More Maintainable

| Layer                  | Recommended Tool              | Why It's Better for NGOs                          | Difficulty |
|------------------------|-------------------------------|----------------------------------------------------|----------|
| Firewall/Router        | **OPNsense** or **pfSense**   | Excellent web interface, VPN, captive portal      | Medium   |
| Virtualization         | **Proxmox VE**                | Run multiple servers on one machine               | Medium   |
| File Sharing & Cloud   | **Nextcloud**                 | Modern replacement for the old cloud backup       | Easy     |
| HR & Admin             | **ERPNext** or **OrangeHRM**  | Full HR + Leave + Appraisal + Payroll             | Medium   |
| Internal Email         | **Mailcow** or **Nextcloud Mail** | Works offline on local network                 | Medium   |
| Library System         | **Koha** or **Calibre Web**   | Proper library management                         | Medium   |
| Storage                | **TrueNAS SCALE**             | Successor to FreeNAS with better apps             | Medium   |

### Recommended Hardware (Low-Cost)

- 1 powerful server (Intel i5/i7, 16–32GB RAM, 500GB+ SSD + HDDs) → Run Proxmox
- 1 smaller machine for pfSense/OPNsense
- POE Switch (8 or 16 port)
- Good UPS for power protection (very important in Nigeria)

### High-Level Implementation Steps

1. **Network Foundation**
   - Install OPNsense/pfSense as main gateway
   - Configure DHCP, DNS, Captive Portal, VPN
   - Set up wired + wireless (separate SSIDs recommended: Staff & Guests)

2. **Core Server Setup (Proxmox recommended)**
   - Install Proxmox VE
   - Create VMs/LXC containers:
     - Nextcloud (File sharing + collaboration)
     - ERPNext or OrangeHRM (HR system)
     - Mail server

3. **Storage & Backup**
   - Set up TrueNAS or use Nextcloud with external storage
   - Enable snapshots and regular backups

4. **User Access**
   - Central dashboard (can be a simple webpage or Nextcloud)
   - Single Sign-On where possible

5. **Security & Maintenance**
   - Strong passwords + 2FA
   - Regular updates
   - Train at least 2 staff members on basic maintenance

### Cost-Saving Tips (Same Philosophy as 2017)

- Use refurbished/used enterprise hardware from Lagos markets (Computer Village)
- Buy POE switch once — future-proofs for IP phones & CCTV
- Prefer open-source over paid licenses
- Start small: Network + Nextcloud + HR first, then expand

### Training & Change Management

- Create simple user manuals with screenshots
- Conduct hands-on training sessions
- Appoint an internal ICT champion
- Start with enthusiastic staff first

**Original GPI Calabar User Manual** has been rewritten in a generic, privacy-safe version below.
