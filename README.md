# OWASP Juice Shop — Task 1 Security Assessment

- **Author:** NIVAS.B.U
- **Date:** 2025-10-19

## Summary
This repository contains a Security Assessment Report (Task 1) for a local deployment of the OWASP Juice Shop web application. The report documents manual testing, verified PoCs, and remediation recommendations for web application vulnerabilities identified during the assessment.

## Key Findings (high level)
- SQL Injection (High)  
- Sensitive Data Exposure (Medium)  
- Persistent (Stored) XSS (High)  
- Reflected XSS (Medium–High)  
- DOM XSS (Medium)  
- Broken Authentication (Medium–High)  
- Broken Access Control  (High)

## Files
- `Security_Assessment_Report.pdf` — Full PDF report .  


## Environment
- Local Docker container running OWASP Juice Shop (HTTP on port 3000).  
- Host OS used to run Docker and testing: *(specify your OS if desired, e.g., Windows 11 / Ubuntu 22.04)*.

## Tools used
- Burp Suite (Community) — proxy, Repeater, request capture.  
- Firefox Developer Tools — DOM inspection, network, screenshots.  
- curl — quick HTTP checks.  
- Docker — containerized app runtime.  
- Optional: OWASP ZAP, Nikto.

## Quick reproduction (run locally)
```bash
# pull & run Juice Shop (runs on http://localhost:3000)
docker run --rm -d --name juice-shop -p 3000:3000 bkimminich/juice-shop

# verify
curl -I http://localhost:3000
```

## How I tested (brief)

- Started Juice Shop in Docker and configured a browser to proxy through Burp.
- Performed reconnaissance to map endpoints and input points.
- Used Burp Repeater to craft PoCs (XSS, SQLi) and validated stored/reflected DOM behaviors.
- Collected raw requests and screenshots as evidence, and documented remediation steps

## Notes for reviewers
- All testing was performed in a local lab environment and was non-destructive.

