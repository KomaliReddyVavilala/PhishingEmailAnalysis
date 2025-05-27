# Phishing Email Analysis Report

## Objective
To analyze a simulated phishing email and identify key characteristics that indicate it is malicious, with special attention to blacklist status, spoofing, and failed authentication.

---
##  Email Summary

- From: support@netflx-billing.com  
- To: user@example.com  
- Subject: [Action Required] Your Payment Failed!  
- IP Address: 185.244.25.92  
- Email Tool Used: PHPMailer  

---

##  Finding the Phishing 

### 1. Fake Email Address  
- The sender's email looks like Netflix but is fake.  
- Real Netflix emails come from `@netflix.com`, not `@netflx-billing.com`.

### 2. Suspicious Link  
- The message says: "Update your billing information"  
- But the link goes to: `http://netflx-billing-login.com`  
- This is not the real Netflix website.

### 3. Failed Security Checks  
- The email failed SPF, DKIM, and DMARC.  
- These are security checks to prove the email is really from the company.  
- Failing them means the email is likely fake or spoofed.

### 4. Urgent Language  
- The email says "Payment is Failed" and "avoid service interruption".  
- This creates panic so that you quickly click the link without thinking.

### 5. IP is Blacklisted  
- The IP address `185.244.25.92` is known to send bad emails.  
- It is on email blacklists used by security systems.

---

##   Conclusion

This email is a phishing attempt. It is:
- Using a fake sender
- Has a dangerous link
- Fails all security checks
- Uses panic and fear to trick the user

---

## Tools Used

- Manual Tool Box for Header Analyzer
- Manual check: Looked at links, language, and sender info

---

## Advice

- Never click unknown links.
- Always check the sender’s email address.
- Report emails like this to your IT or security team.

