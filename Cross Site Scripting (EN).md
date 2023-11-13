# Cross Site Scripting (XSS)

Severity: Medium  
CVSS: 4.6, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:R/S:U/C:L/I:L/A:N&version=3.1

## Affected Assets

CHANGE ME!

## Description

The web application is vulnerable to Cross-site scripting (XSS) attacks, which enable attackers to inject client-side scripts into web pages viewed by other users.

This vulnerability arises when input validation is not properly done. As a consequence, the malicious data will appear to be part of the web site and run within the user's browser under the privileges of the web application.

This vulnerability can be used to conduct several browser-based attacks including:

* Hijacking another user's browser
* Capturing sensitive information viewed by application users
* Pseudo defacement of the application
* Port scanning of internal hosts ("internal" in relation to the users of the web application)
* Directed delivery of browser-based exploits
* Other malicious activities


## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to always validate all inputs. NEVER TRUST user input.

Please refer to https://en.wikipedia.org/wiki/Cross-site_scripting#Preventive_measures.

## Reference

* OWASP Testing Guide (WSTG-INPV-01), reflected XSS, https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/01-Testing_for_Reflected_Cross_Site_Scripting
* OWASP Testing Guide (WSTG-INPV-02), stored XSS, https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/02-Testing_for_Stored_Cross_Site_Scripting
* OWASP Testing Guide (WSTG-CLNT-01), DOM-based XSS, https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/01-Testing_for_DOM-based_Cross_Site_Scripting
* PortSwigger, https://portswigger.net/web-security/cross-site-scripting
