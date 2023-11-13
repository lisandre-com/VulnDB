# Cross Site Request Forgery (CSRF)

Severity: Medium  
CVSS: 5.4, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:U/C:L/I:L/A:N&version=3.1

## Affected Assets

CHANGE ME!

## Description

Cross-Site Request Forgery (CSRF) is an attack that forces an end user to execute unintended actions on a web application in which they are currently authenticated. With a little social engineering help (like sending a malicious link via email or chat), an attacker may force the users of a web application to execute actions of the attacker's choosing. A successful CSRF exploit can compromise end user data and operation when it targets a normal user. If the targeted end user is the administrator account, a CSRF attack can compromise the entire web application.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to protect ALL sensitive functionalities against CSRF. Refer to https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html.

## Reference

* OWASP Testing Guide (WSTG-SESS-05), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/06-Session_Management_Testing/05-Testing_for_Cross_Site_Request_Forgery
* PortSwigger, https://portswigger.net/web-security/csrf
