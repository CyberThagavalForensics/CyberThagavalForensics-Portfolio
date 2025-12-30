# Case 3: Email Header Phishing Detection

**Scenario**  
Analysis of a suspicious email header to identify phishing indicators and trace the real sender.

**Sample Email Header Used**  
Reconstructed from common public phishing examples (synthetic for demonstration – no real email).

**Tools Used**  
- Manual header parsing  
- MX Toolbox (SPF/DKIM check)  
- WhoIs & IP geolocation lookup

**Key Findings**  
- "From" address spoofed: Display name "SBI Bank" but sender domain @random-domain.xyz  
- X-Originating-IP: IP from Nigeria (not official SBI server range)  
- SPF check: Fail (sender not authorized)  
- DKIM signature: Missing  
- Reply-to address different from From → redirect replies to attacker  
- Embedded link pointed to phishing site (hxxp://sbi-login[.]xyz)

**Conclusion**  
Even sophisticated phishing emails can be detected quickly by examining headers for spoofing, authentication failures, and mismatched domains/IPs. Always verify before clicking links or sharing OTP.

**Disclaimer**  
This is a sample analysis using reconstructed public phishing header data for portfolio demonstration only. No real client email or PII involved.
