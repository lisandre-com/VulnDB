# Sensitive information exposed (Web server version)

Severity: Info  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

The web server reveals information on its version. Exposed server information can assist attackers in exploiting other vulnerabilities that may exist. It can also lead attackers to find version-specific server vulnerabilities that can be used to exploit unpatched servers.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to remove version information from the web server headers.

While exposed server information is not necessarily in itself a vulnerability, it is information that can assist attackers in exploiting other vulnerabilities that may exist. Exposed server information can also lead attackers to find version-specific server vulnerabilities that can be used to exploit unpatched servers. For this reason it is recommended that some precautions be taken. These actions include:

* Remove web server information from headers, such as with Apache’s mod_headers module.

* Using a hardened reverse proxy server to create an additional layer of security between the web server and the Internet.

* Ensuring that web servers are kept up-to-date with the latest software and security patches.

## Reference

* OWASP Testing Guide (WSTG-INFO-02), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/01-Information_Gathering/02-Fingerprint_Web_Server
