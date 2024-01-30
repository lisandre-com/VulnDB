# Open Redirection

Severity: Low  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

Open redirection vulnerabilities arise when an application incorporates user-controllable data into the target of a redirection in an unsafe way. An attacker can construct a URL within the application that causes a redirection to an arbitrary external domain. This behavior can be leveraged to facilitate phishing attacks against users of the application. The ability to use an authentic application URL, targeting the correct domain and with a valid SSL certificate (if SSL is used), lends credibility to the phishing attack because many users, even if they verify these features, will not notice the subsequent redirection to a different domain.

Open redirections can be stored or reflected.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to validate user input to restrict which URLs are allowed. Ideally, the application workflow should not depend on data that originated from any untrusted source.

## Reference

* OWASP Testing Guide (WSTG-CLNT-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/04-Testing_for_Client-side_URL_Redirect
* PortSwigger, https://portswigger.net/web-security/dom-based/open-redirection
