# SAML Attacks

Severity: High  
CVSS: 8.8, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:N/S:U/C:H/I:H/A:H&version=3.1

## Affected Assets

CHANGE ME!

## Description

The Security Assertion Markup Language (SAML) is an open standard for exchanging authorization and authentication information.

**Signature Validation Bypass**: when a signature is not validated (ignored) in the SAMLResponse, attackers can manipulate the content of an XML document without detection. In this scenario, the system blindly trusts the data in the document, allowing attackers to inject malicious or unauthorized information - like changing the username, groups, roles, etc. This can lead to serious security breaches, such as bypassing authentication, gaining unauthorized access, or tampering with critical data, as the absence of signature validation leaves the system vulnerable to any form of manipulation.

**XML Signature Wrapping (XSW)**: the attacker modifies an XML document by moving or duplicating parts of the signed data while leaving the digital signature intact, tricking the system into processing malicious content as if it were trusted. This exploits the discrepancy between how different parts of the system validate the signature and process the XML data, allowing attackers to bypass authentication or authorization checks.

**SAML XML External Entity (XXE)**: attacks that exploit vulnerabilities in XML parsers by injecting malicious external entities into SAML messages, potentially leading to data exfiltration, denial of service, or server-side request forgery.

## Supporting Evidence

CHANGE ME!

## Recommendation

**Signature Validation Bypass**: Always validate SAML signatures. Follow recommendations from OWASP (see reference below).

**XML Signature Wrapping (XSW)**: Use strong XML signature validation libraries, enforce proper XML canonicalization, and validate the schema to ensure message integrity. Limit where signed assertions are accepted, verify unique references, and check that only intended data is signed. Validate trust relationships using metadata, and regularly update your SAML libraries. Logging and monitoring can also help detect unusual behavior and potential attacks early. Follow recommendations from OWASP (see reference below).

**SAML XML External Entity (XXE)**: To prevent these attacks, disable external entity resolution in XML parsers, use secure and up-to-date parsing libraries, validate incoming SAML messages, and only accept messages from trusted sources. These measures help safeguard against XXE vulnerabilities in SAML implementations.

## Reference

* OWASP SAML Security Cheat Sheet, https://cheatsheetseries.owasp.org/cheatsheets/SAML_Security_Cheat_Sheet.html
* SAML Attacks, https://book.hacktricks.xyz/pentesting-web/saml-attacks
