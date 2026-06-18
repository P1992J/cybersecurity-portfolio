# ISO 27001 Gap Analysis — Home Network Environment

**Analyst:** Julita Patel  
**Platform:** Personal Portfolio Project  
**Category:** GRC Analysis  
**Standard:** ISO/IEC 27001:2022  
**Date:** June 2026  
**Scope:** Home network environment — Laptop, Smartphone, WiFi Router (Netgear Orbi), Cloud Accounts  

---

## Scenario

This project applies ISO 27001 information security principles to a real home network environment, treating it as a small company environment. The goal is to identify security control gaps, assess risk, and produce a prioritised improvement plan — demonstrating practical GRC thinking applicable to any organisation.

ISO 27001 is the international standard for Information Security Management Systems (ISMS). It defines a risk-based approach to protecting the confidentiality, integrity, and availability of information.

---

## Tools Used

- ISO/IEC 27001:2022 framework
- Microsoft Excel — gap analysis table and scoring
- Netgear Orbi router admin panel
- Google Account Security dashboard
- Manual assessment methodology

---

## Scope Definition

| Asset | Type | Data Classification |
|-------|------|-------------------|
| Laptop | Endpoint device | Personal data, work documents, browser credentials |
| Smartphone | Mobile device | Personal data, financial apps, photos, communications |
| Home WiFi Router (Netgear Orbi) | Network infrastructure | Controls all internet traffic |
| Gmail Account | Cloud account | Personal and professional email communications |
| Cloud Storage | Cloud account | Documents, photos, backups |

---

## Assessment Methodology

Each control area was assessed against ISO 27001 good practice using a three-point scoring system:

| Score | Meaning |
|-------|---------|
| ✅ Met | Control exists and is working effectively |
| ⚠️ Partial | Some evidence of control but gaps remain |
| ❌ Not Met | Control is missing or unclear |

---

## Gap Analysis Results

### Control 1 — Asset Management
**Score: ✅ Met**

| Check Point | Status | Notes |
|-------------|--------|-------|
| Complete inventory of all devices | ✅ Met | Laptop, phone, router documented |
| Complete inventory of all accounts | ✅ Met | Gmail, cloud storage, social media documented |

**Finding:** Asset inventory is complete and up to date. All devices and accounts have been identified and documented.

**Recommendation:** Review and update inventory quarterly or when new devices are added.

---

### Control 2 — Access Control
**Score: ⚠️ Partial**

| Check Point | Status | Notes |
|-------------|--------|-------|
| Strong password on laptop | ✅ Met | Strong password in place |
| PIN/fingerprint on smartphone | ✅ Met | Biometric and PIN protection active |
| Unique passwords per account | ✅ Met | Different passwords used across accounts |
| Two-factor authentication on Gmail | ❌ Not Met | 2FA not currently enabled |

**Finding:** Access controls are strong across devices but two-factor authentication is not enabled on the primary email account. This represents a significant risk — if the Gmail password is compromised, an attacker gains full account access with no additional barrier.

**Recommendation — High Priority:**
Enable 2FA on Gmail immediately:
1. Go to myaccount.google.com
2. Click Security
3. Click 2-Step Verification
4. Follow the setup steps

---

### Control 3 — System Security
**Score: ✅ Met**

| Check Point | Status | Notes |
|-------------|--------|-------|
| Laptop operating system up to date | ✅ Met | Windows updates current |
| Antivirus installed and active | ✅ Met | Endpoint protection in place |
| Smartphone software up to date | ✅ Met | Mobile OS fully patched |

**Finding:** All devices are patched and protected. Antivirus is active on the laptop and all software is current.

**Recommendation:** Enable automatic updates on all devices to maintain patch status without manual intervention.

---

### Control 4 — Network Security
**Score: ✅ Met**

| Check Point | Status | Notes |
|-------------|--------|-------|
| WiFi network password protected | ✅ Met | WPA2/WPA3 encryption in place |
| Router admin password changed from default | ✅ Met | Default credentials replaced |
| Guest network available for visitors | ✅ Met | Visitors isolated from main network |

**Finding:** Network security is well configured. The Netgear Orbi router has been properly secured with a non-default admin password and a guest network is available to isolate visitor traffic from primary devices.

**Recommendation:** Periodically review connected devices in the Orbi admin panel to identify any unauthorised connections.

---

### Control 5 — Backups and Recovery
**Score: ⚠️ Partial**

| Check Point | Status | Notes |
|-------------|--------|-------|
| Laptop files backed up | ✅ Met | Backup solution in place |
| Phone photos backed up automatically | ⚠️ Partial | Some photos backing up but not all |
| Backup restore tested | ✅ Met | Restore has been verified |

**Finding:** Laptop backup is in place and has been tested. However, phone photo backup is only partial — not all photos are automatically backed up, creating a risk of permanent data loss if the device is lost or damaged.

**Recommendation — Medium Priority:**
Enable full Google Photos backup:
1. Open Google Photos app
2. Go to Settings
3. Select Backup
4. Turn on Backup and select Back up all photos

---

### Control 6 — Incident Response
**Score: ⚠️ Partial**

| Check Point | Status | Notes |
|-------------|--------|-------|
| Clear plan if device is compromised | ⚠️ Partial | No documented plan exists |
| Know who to contact during incident | ⚠️ Partial | No contact list documented |
| Know how to isolate a compromised device | ✅ Met | Can disconnect device from network |

**Finding:** Basic isolation capability exists but no formal incident response plan or contact list is documented. Without a clear plan, response time increases and potential damage worsens during a real incident.

**Recommendation — High Priority:**
Create and save an Incident Response Checklist. See the Improvement Plan section below.

---

## Summary of Findings

| Control Area | Score | Priority |
|-------------|-------|---------|
| 1. Asset Management | ✅ Met | — |
| 2. Access Control | ⚠️ Partial | 🔴 High — Enable Gmail 2FA |
| 3. System Security | ✅ Met | — |
| 4. Network Security | ✅ Met | — |
| 5. Backups and Recovery | ⚠️ Partial | 🟡 Medium — Full phone backup |
| 6. Incident Response | ⚠️ Partial | 🔴 High — Create IR checklist |

**Overall posture: Good — with three targeted improvements needed**

---

## Improvement Plan

| Priority | Gap | Action | Effort |
|----------|-----|--------|--------|
| 🔴 High | Gmail 2FA not enabled | Enable 2-Step Verification on Google account | 5 minutes |
| 🔴 High | No incident response plan | Create and save IR checklist with CERT NZ contact | 30 minutes |
| 🟡 Medium | Phone photos not fully backed up | Enable full Google Photos automatic backup | 5 minutes |
| 🟢 Low | No quarterly asset review | Schedule quarterly review of devices and accounts | Ongoing |

---

## Incident Response Checklist

In the event of a suspected security incident:

1. **Detect** — Identify unusual activity, alerts, or device behaviour
2. **Disconnect** — Turn off WiFi on affected device immediately
3. **Isolate** — Enable Airplane Mode or unplug ethernet cable
4. **Assess** — From a different device, check which accounts may be affected
5. **Change Passwords** — Update passwords for Gmail and critical accounts from a safe device
6. **Revoke Access** — Review active sessions: myaccount.google.com → Security → Manage Devices
7. **Report** — Contact CERT NZ: cert.govt.nz | report@cert.govt.nz | 0800 CERTNZ
8. **Scan** — Run a full antivirus scan before reconnecting the device
9. **Reconnect** — Only reconnect after scan returns clean
10. **Document** — Record what happened, when, and what actions were taken

**Key Contact:** CERT NZ — cert.govt.nz | report@cert.govt.nz | 0800 CERTNZ

---

## Key Learnings

- How to apply ISO 27001 controls to a real environment
- How to score compliance gaps using Met / Partial / Not Met methodology
- How to assess risk and prioritise remediation actions
- How to produce a structured GRC gap analysis report
- The importance of two-factor authentication as a first-line control
- How to create a practical incident response plan for a home environment

---

## MITRE ATT&CK Relevance

The gaps identified map to the following MITRE ATT&CK techniques that attackers commonly exploit:

| Gap | MITRE Technique | Tactic |
|-----|----------------|--------|
| No Gmail 2FA | T1078 — Valid Accounts | Initial Access |
| No IR plan | T1486 — Data Encrypted for Impact | Impact |
| Partial backups | T1490 — Inhibit System Recovery | Impact |

---

*This analysis was completed as part of a personal GRC analyst portfolio project.*  
*Analyst: Julita Patel | julitakpatel@gmail.com | Wellington, New Zealand*  
*GitHub: github.com/P1992J/julita-patel-portfolio*


