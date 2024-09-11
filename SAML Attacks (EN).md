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

**Signature Validation Bypass**:

Always validate SAML signatures. Follow recommendations from OWASP (see reference below).

**XML Signature Wrapping (XSW)**:

* **Use secure XML signature validation libraries**: Utilize strong XML signature validation libraries to ensure that the signed data matches the intended elements, preventing attackers from bypassing security checks.
* **Apply proper XML canonicalization**: Canonicalize XML data to create a consistent structure, ensuring that any variations in XML format are neutralized and preventing exploitation of those differences.
* **Enforce XML schema validation**: Validate all SAML messages against the correct XML schema to block the introduction of malicious or unexpected elements used in XSW attacks.
* **Restrict signed data locations**: Limit where signed elements can appear in XML messages to prevent attackers from moving valid signatures to different parts of the message.
* **Check unique element references**: Ensure XML elements referenced by signatures are unique and properly linked to prevent duplication or manipulation used in XSW attacks.
* **Verify entire message integrity**: Check the structure and integrity of the entire XML message, ensuring that the signed portions cover the correct data and nothing is altered.
* **Transmit messages securely**: Use secure methods like HTTP POST with TLS to protect the SAML message during transmission, reducing the chance of manipulation in transit.

**SAML XML External Entity (XXE)**:

To prevent these attacks, disable external entity resolution in XML parsers, use secure and up-to-date parsing libraries, validate incoming SAML messages, and only accept messages from trusted sources. These measures help safeguard against XXE vulnerabilities in SAML implementations.

## Reference

* OWASP SAML Security Cheat Sheet, https://cheatsheetseries.owasp.org/cheatsheets/SAML_Security_Cheat_Sheet.html
* SAML Attacks, https://book.hacktricks.xyz/pentesting-web/saml-attacks
