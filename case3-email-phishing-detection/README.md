# Case 3: Email Header Phishing Detection

**Scenario**  
Analysis of a suspicious email claiming to be from SBI, requesting account verification.

**Email Details**  
- From: communications.sbi.co.in (spoofed)  
- Subject: Explore Smarter Payments & Easier Withdrawals With Yono SBI  
- Received: 18 August 2025

**Tools Used**  
- Gmail "Show Original" for header extraction  
- MX Toolbox Email Header Analyzer

**Key Findings**  
- SPF: Fail  
- DKIM: Fail  
- DMARC: Fail  
- Received From IP: 175.158.69.24 (not official SBI server range)  
- Return-Path mismatched with From address  
- Sending IP in Spamhaus blacklist  
- IP Geolocation: Eastern Europe (not India/SBI official)  
- All authentication checks failed → high phishing indicator

**Conclusion**  
The analyzed mail is fake/phishing. It did not originate from SBI servers and failed all authentication tests (SPF, DKIM, DMARC). This confirms the mail is a spoofed spam message and should not be trusted.

**Screenshots**  
- See /screenshots folder for:  
  Gmail Show Original, authentication results, header fields, MX Toolbox analysis

**Disclaimer**  
This is a sample analysis of a real suspicious email for portfolio demonstration only. No sensitive PII shared; headers anonymized where needed.
