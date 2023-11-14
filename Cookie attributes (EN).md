# Cookie attributes

Severity: Varies  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

A cookie is a small piece of data that a server sends to the user’s web browser. The browser may store it and send it back with later requests to the same server. Typically, it’s used to tell if two requests came from the same browser – keeping a user logged-in, for example. It remembers stateful information for the stateless HTTP protocol. Cookies are often a key attack vector for malicious users (typically targeting other users) and the application should always take due diligence to protect cookies.

A cookie with the Secure attribute is sent to the server only with an encrypted request over the HTTPS protocol, never with unsecured HTTP (except on localhost), and therefore can’t easily be accessed by a man-in-the-middle attacker. Insecure sites (with http: in the URL) can’t set cookies with the Secure attribute. However, do not assume that Secure prevents all access to sensitive information in cookies; for example, it can be read by someone with access to the client's hard disk.

A cookie with the HttpOnly attribute is inaccessible to the JavaScript Document.cookie API; it is sent only to the server. For example, cookies that persist server-side sessions don’t need to be available to JavaScript, and should have the HttpOnly attribute. This precaution helps mitigate Cross-Site Scripting (XSS) attacks.

The SameSite attribute is used to assert that a cookie ought not to be sent along with cross-site requests. This feature allows the server to mitigate the risk of cross-origin information leakage. In some cases, it is used too as a risk reduction (or defense in depth mechanism) strategy to prevent cross-site request forgery attacks.


## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to review cookie configurations:

* Set the HttpOnly flag
* Set a reasonable expiration date
* Set the SameSite attribute

## Reference

* OWASP Testing Guide (WSTG-SESS-02), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/06-Session_Management_Testing/02-Testing_for_Cookies_Attributes
* PortSwigger, https://portswigger.net/kb/issues/00500200_tls-cookie-without-secure-flag-set
* PortSwigger, https://portswigger.net/kb/issues/00500300_cookie-scoped-to-parent-domain
* PortSwigger, https://portswigger.net/kb/issues/00500600_cookie-without-httponly-flag-set
