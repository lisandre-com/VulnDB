# Clickjacking (UI redressing)

Severity: Medium  
CVSS: 6.1, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N

## Affected Assets

CHANGE ME!

## Description

The web application is vulnerable to Clickjacking attacks. Clickjacking is when an attacker uses multiple transparent or opaque layers to trick a user into clicking on a button or link on another page when they were intending to click on the top-level page. Thus, the attacker is "hijacking" clicks meant for their page and routing them to another page, most likely owned by another application, domain, or both.

Using a similar technique, keystrokes can also be hijacked. A user can be led to believe they are typing in their credentials (username, password) into the web application, but are instead typing into an invisible frame controlled by the attacker.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to prevent clickjacking by sending the proper Content Security Policy (CSP) frame-ancestors directive response headers that instruct the browser to not allow framing from other domains. This replaces the older X-Frame-Options HTTP headers according to OWASP.

## Reference

* OWASP Testing Guide (WSTG-CLNT-09), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/09-Testing_for_Clickjacking
* PortSwigger, https://portswigger.net/web-security/clickjacking
