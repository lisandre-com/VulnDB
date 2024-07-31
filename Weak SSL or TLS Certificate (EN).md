# Weak SSL/TLS Certificate

Severity: Medium  
CVSS: 6.1, https://nvd.nist.gov/vuln-metrics/cvss/v2-calculator?vector=(AV:N/AC:H/Au:N/C:C/I:P/A:N)
(based on scanner)

## Affected Assets

CHANGE ME!

## Description

TLS version 1.0 is enabled and the server supports at least one cipher. TLS 1.0 has a number of cryptographic design flaws. Modern implementations of TLS 1.0 mitigate these problems, but newer versions of TLS like 1.2 and 1.3 are designed against these flaws and should be used whenever possible.

TLS version 1.1 is enabled and the server supports at least one cipher. TLS 1.1 lacks support for current and recommended cipher suites. Ciphers that support encryption before MAC computation, and authenticated encryption modes such as GCM cannot be used with TLS 1.1.

As of March 31, 2020, endpoints that are not enabled for TLS 1.2 and higher will no longer function properly with major web browsers and major vendors.

## Supporting Evidence

CHANGE ME!

## Recommendation

Enable support for TLS 1.2 and 1.3, and disable support for TLS 1.0 and TLS 1.1.

## Reference

* OWASP Testing Guide (WSTG-CRYP-01), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/09-Testing_for_Weak_Cryptography/01-Testing_for_Weak_Transport_Layer_Security
* OWASP Cheat Sheet, https://cheatsheetseries.owasp.org/cheatsheets/Transport_Layer_Security_Cheat_Sheet.html
* PortSwigger, https://portswigger.net/kb/issues/01000100_tls-certificate
