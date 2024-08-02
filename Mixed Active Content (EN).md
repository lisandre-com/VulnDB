# Mixed Active Content (HTTP + HTTPS)

Severity: Info  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

_Mixed Active Content_ is when active resources (such as scripts to CSS) are loaded over unencrypted HTTP and included into a secure (HTTPS) page. This is dangerous because it would allow an attacker to modify these files (as they are sent unencrypted), which could allow them to execute arbitrary code (JavaScript or CSS) in the page. Passive content (such as images) loaded over an insecure connection can also leak information or allow an attacker to deface the page, although it is less likely to lead to a full compromise.

_Note: Modern browsers will block active content being loaded from insecure sources into secure pages._

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to only access ressources over HTTPS in applications using HTTPS (no mix of HTTP and HTTPS requests in the application).

## Reference

* OWASP Testing Guide (WSTG-CRYP-01), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/09-Testing_for_Weak_Cryptography/01-Testing_for_Weak_Transport_Layer_Security
