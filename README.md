# Phishing Email Investigation Lab
**Date:** January 30, 2026
**Analyst:** Triumph Izegaegbe


## Objective
To analyze a suspected phishing email, identify indicators of compromise, and assess the associated organizational risk.


## Tools Used
- Ubuntu VM
-  Email Dataset
- Sublime text
- WHOIS / Domain Intelligence Lookup


## Investigation Steps
1. Examined sender email address for spoofing patterns.
2. Performed full header analysis using Sublime text.
3. Reviewed SPF, DKIM and DMARC authentication results.
4. Inspected embedded links for malicious redirection.
5. Evaluated email language for social engineeering tactics.


## Findings
1. The sender domain exhibited characteristics consistent with spoofing and did not align with legitimate organizational infrastructure.
2. The IP registration details did not align with the organization the sender claimed to represent.
3. Email authentication analysis resulted in SPF, DKIM, and DMARC failure, providing high-confidence evidence of sender illegitimacy.
4. The embedded hyperlink directed users to a webpage served over HTTP rather than HTTPS, meaning the connection lacked transport-layer encryption.
5. The greeting "Dear wamu.com customer" was indeed too generic.
6. Wrong grammar was detected in the email content.


## Indicators of Compromise (IOCs)
1. Suspicious sender address (debit-request-updaxh@wamu.com)
2. Unverified Originating IP (61.42.125.43)
3. Possible credential harvesting URL
4. Urgency-Based language
5. Generic greeting
6. Grammar errors


## Risk Assessment
The analyzed email presents a high probability of phishing and poses a significant risk to both individual users and organizational environments. Multiple high-confidence indicators such as an unencrypted credential portal and social engineering tactics, strongly suggest malicous intent.
Given the high likelihood of user interaction and the severe potential impact of credential theft, the overall risk was determined to be Critical.


## Recommended Actions
1. Block malicious domain at the email gateway.
2. Alert users about phishing attempt.
3. Quarantine or delete all copies of the phishing email.
4. Reset affected credentials.
5. Enforce Multi-Factor authentication.
6. Implement advanced email-filtering.
7. Enable domain authentication.


## Key Takeaways
The email represents a low-sophistication phishing attempt. While the attack contained several easily identifiable indicators, it still posed a measurable risk to unsuspecting users, highlighting that even poorly executed phishing campaigns can result in credential compromise.


## Analyst Conclusion
This investigation identified multiple high-confidence indicators consistent with phishing, including authentication failures, unauthorized infrastructure, and an unencrypted credential portal.
Although the attack demonstrated low sophistication, the potential impact remained severe if successful. Immediate containment and preventive controls are recommended to reduce organizational exposure.


## Data Source
Public phishing email dataset obtained from Academic Torrents (https://academictorrents.com/details/a77cda9a9d89a60dbdfbe581adf6e2df9197995a)
Used strictly for educational and cybersecurity training purposes.
