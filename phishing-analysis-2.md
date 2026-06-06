# Phishing Analysis 2 — Blue Team Labs Online

**Platform:** Blue Team Labs Online  
**Category:** Phishing Analysis  
**Difficulty:** Easy  
**Date:** 6 June 2026  

---

## Scenario

A phishing email impersonating Amazon was submitted to the SOC for investigation. The email claimed the recipient's account had been locked and urged them to click a button to review their account within 72 hours.

---

## Tools Used

- Mozilla Thunderbird
- Browserling.com
- Base64 Decoder
- Manual header analysis

---

## Key Findings

- **Sending address:** amazon@zyevantoby.cn — spoofed Amazon sender
- **Recipient:** saintington73@outlook.com
- **Subject:** Your Account has been locked
- **Originating IP:** 45.156.23.138
- **Phishing URL:** https://amaozn.zzyuchengzhika.cn/?mailtoken=saintington73@outlook.com
- **Company imitated:** Amazon
- **Encoding:** Email body encoded in Base64 to evade security filters
- **Logo source:** Amazon logo hosted on Squarespace CDN — not Amazon servers
- **Tracking:** Victim email embedded as mailtoken parameter in phishing URL
- **Facebook username linked in email:** amir.boyka.7
- **Verdict:** Confirmed phishing email impersonating Amazon

---

## Key Learnings

- How to identify Base64 encoding using the Content-Transfer-Encoding header
- How to decode Base64 encoded email bodies to extract hidden URLs
- How to extract original URLs from Microsoft SafeLinks wrapped links
- How to identify typosquatting domains (amaozn vs amazon)
- How to safely view suspicious URLs using Browserling.com
- How to identify mailtoken tracking parameters in phishing URLs
