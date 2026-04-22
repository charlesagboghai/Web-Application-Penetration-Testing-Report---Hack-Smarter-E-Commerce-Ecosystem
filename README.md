# Web-Application-Penetration-Testing-Report---Hack-Smarter-E-Commerce-Ecosystem
 # Hack Smarter E-Commerce Ecosystem
# Overview
This report presents the results of a web application penetration test conducted against the Hack Smarter Lab environment on the 2nd April 2026 to 5th of April 2026. The assessment was performed to evaluate the security posture of the application and identify vulnerabilities that could be exploited by malicious actors.

The testing was carried out using a structured methodology aligned with industry standards, including the OWASP Testing Guide and OWASP Top 10 framework. A combination of automated tools and manual techniques was used to simulate real-world attack scenarios from an external attacker’s perspective.
During the assessment, multiple security vulnerabilities of varying severity were identified. These included critical issues such as improper input validation and insecure file upload mechanisms, as well as high and medium risk vulnerabilities like cross-site scripting (XSS), clickjacking, insecure direct object references (IDOR), SQLi and missing security controls. If exploited, these vulnerabilities could allow unauthorized access to sensitive data, compromise user accounts, and potentially lead to full system takeover.

 # Target
+ hacksmarter.hsm
+ *hacksmarter.hsm
  
 # Assessment Type
   Grey Box Web Application Penetration Test
   
 # Penetration Tester
   Charles Agboghai Ozor

  # Tools Used
  + Caido (Web traffic monitoring and request modification)
  + Kali Linux (Testing Environment)
  + Burp Suite (Web traffic monitoring and request modification)
  + John The Ripper (Cracking Of Password)
  + Dirsearch (Directory Brute forcing)
  + SQLMap (Detect And Exploit SQL Injection Vulnerabilities)
  + FFUF (Subdomain Enumeration)

  # Findings
   26 separate security findings (4 Critical, 10 High, 11 Medium and 1 Low)
  
  + Critical: Remote Code Execution via Insecure File Upload (Magic Bytes / Signature Bypass)
  + Critical: SQL Injection in Product Search Leading to Credential Disclosure and Administrative Account Compromise
  + Critical: Information Disclosure of Database User Context via SQL Injection (Database Credential Exposure) 
  + Critical: Stored Cross-Site Scripting (XSS) in Forum, Feedback, and Thread Functionality 
  + High: Local File Inclusion (LFI) via Path Traversal in lang Parameter 
  + High: Lack of Registration Rate Limiting / Automated Account Creation Abuse 
  + High: Improper Session Invalidation After Credential Change 
  + High: Cross-Site Request Forgery (CSRF) in Email Change Function with Missing Anti-CSRF Validation 
  + Weak Authentication Controls Susceptible to Password Spraying / Brute Force Attacks 
  + High: Weak Password Policy / Insufficient Password Complexity Enforcement 
  + High: Client-Side Access Control Bypass Leading to Unauthorized Product Purchase 
  + High: Session Fixation Due to Non-Regenerated Session Identifier After Authentication
  + High: Missing Current Password Verification for Sensitive Account Changes 
  + High: Blind Server-Side Request Forgery (SSRF) via Avatar URL Import Functionality
  + Medium: Clickjacking Due to Missing Anti-Framing Protections 
  + Medium: Information Disclosure via Web Server Fingerprinting 
  + Medium: PHP Configuration Information on Development Subdomain 
  + Medium: Absence of Multi-Factor Authentication (MFA) Across Application Authentication Systems 
  + Medium: Sensitive Endpoint Disclosure via Directory Bruteforcing 
  + Medium: Username Enumeration via Authentication Response Discrepancy 
  + Medium: Username Enumeration via Registration Response Disclosure 
  + Medium: HTML Injection in User-Generated Content Fields (Forum, Feedback, and Thread Creation) 
  + Medium: Open Redirect via Unvalidated “next” Parameter in Login Functionality 
  + Medium: Missing HttpOnly Cookie Attribute on Session Cookies 
  + Medium: Insecure Direct Object Reference (IDOR) Allowing Access to Unreleased Products 
  + Low: Absence of CAPTCHA Protection on Public-Facing Forms and Authentication Endpoints

 # Conclusion
   The penetration test identified multiple security vulnerabilities across the web application, including several Critical and High-risk findings that could lead to unauthorized access, account compromise, sensitive data    exposure, and potential full system takeover. Additional Medium and Low severity issues were also observed, indicating weaknesses in security controls and configuration practices.

   Overall, the application’s security posture requires improvement. Immediate remediation of Critical and High findings is recommended, followed by corrective actions for lower-risk issues to reduce overall exposure and     strengthen resilience against future attacks.
    

  


