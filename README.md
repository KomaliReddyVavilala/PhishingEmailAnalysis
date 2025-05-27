# Phishing Email Analysis: Netflix Payment Scam

##  Project Overview
Analysis of a phishing email impersonating Netflix's billing department, including:
- Full email header analysis
- Authentication protocol verification
- Blacklist status checks
- Behavioral red flags identification


##  Key Findings
| Indicator               | Evidence                                  | Impact  |
|-------------------------|------------------------------------------|---------|
| Domain Spoofing         | `netflx-billing.com` (missing 'i')       | High    |
| Authentication Failure  | SPF/DKIM/DMARC all failed                | Critical|
| Blacklisted IP          | 185.244.25.92 (known malicious)          | Critical|
| Urgency Tactics         | "Payment is Failed" subject              | Medium  |
| Suspicious Link         | `netflx-billing-login.com`               | High    |

##  Analysis Tools
1. Header Analysis
   - Manual inspection of email headers
   - SPF/DKIM/DMARC verification
2. IP Reputation
   - AbuseIPDB lookup
   - Spamhaus blacklist check
3. Domain Analysis
   - WHOIS registration check
   - VirusTotal scan

##  Safety Recommendations
-  Never click links in payment request emails
-  Always manually type Netflix.com instead of clicking links
-  Forward phishing attempts to: phishing@netflix.com
-  Check sender addresses carefully for misspellings

##  How to Use These Files
1. For Security Professionals:
   - Review `headerAnalysis.txt` for forensic patterns
   - Cross-reference IP 185.244.25.92 with current blacklists
2. For Learners:
   - Study `phishing_analysis.md` for detection methodology
   - Compare real vs fake Netflix email headers
3. For Developers:
   - Use screenshots as reference for building detection systems
   - Adapt analysis techniques for security applications

##  Credits
- Email sample analysis performed using:
  - MXToolBox Header Analyzer
  - Manual forensic examination
- Blacklist verification via AbuseIPDB

---
