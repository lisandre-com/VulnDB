# Insecure Direct Object References (IDOR)

Severity: Varies  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

Insecure Direct Object References (IDOR) occur when an application provides direct access to objects based on user-supplied input. It allows attackers to bypass authorization and access resources directly by modifying the value of a parameter used to directly point to an object.

This is caused by the fact that the application takes user supplied input and uses it to retrieve an object without performing sufficient authorization checks.

## Supporting Evidence

CHANGE ME!

## Recommendation

Ensure that each use of a direct object reference has proper access control checks to verify that a user has permission to access the requested resource.

## Reference

* OWASP Testing Guide (WSTG-ATHZ-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/05-Authorization_Testing/04-Testing_for_Insecure_Direct_Object_References
