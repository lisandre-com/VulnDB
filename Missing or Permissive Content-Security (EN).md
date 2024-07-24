# Missing or Permissive Content-Security-Policy (CSP) HTTP Header

Severity: Info  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

Content Security Policy (CSP) is a declarative allow-list policy enforced through Content-Security-Policy response header or equivalent <meta> element. It allows developers to restrict the sources from which resources such as JavaScript, CSS, images, files etc. are loaded. CSP is an effective defense in depth technique to mitigate the risk of vulnerabilities such as Cross Site Scripting (XSS) and Clickjacking.

By injecting the Content-Security-Policy (CSP) headers from the server, the browser is aware and capable of protecting the user from dynamic calls that will load content into the page currently being visited.

When CSP is misconfigured or not set, an attacker might be able to run malicious JavaScript, which could lead to partial compromise of confidentiality and integrity. The exploitability of this flaw depends on whether an attacker can inject JavaScript into the application, or whether any allowed script sources can be abused to host potentially malicious files.

Even on a fully static website, which does not accept any user input, a CSP can be used to enforce the use of Subresource Integrity (SRI). This can help prevent malicious code being loaded on the website if one of the third-party sites hosting JavaScript files (such as analytics scripts) is compromised.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to ensure that the Content Security Policy (CSP) is set and does not contain weak policy configurations, or sources known to host files which can be used to bypass the CSP. Consider the risk associated with allowing "unsafe-inline" and "unsafe-eval" policies.

## Reference

* OWASP Testing Guide (WSTG-CONF-12), https://github.com/OWASP/wstg/blob/master/document/4-Web_Application_Security_Testing/02-Configuration_and_Deployment_Management_Testing/12-Test_for_Content_Security_Policy.md
* OWASP Content Security Policy Cheat Sheet, https://cheatsheetseries.owasp.org/cheatsheets/Content_Security_Policy_Cheat_Sheet.html
