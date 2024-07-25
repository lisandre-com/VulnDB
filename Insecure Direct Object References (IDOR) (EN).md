# Insecure Direct Object References (IDOR)

Severity: Varies  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

Insecure Direct Object References (IDOR) occur when an application provides direct access to objects based on user-supplied input. It allows attackers to bypass authorization and access resources directly by modifying the value of a parameter used to directly point to an object.

This is caused by the fact that the application takes user supplied input and uses it to retrieve an object without performing sufficient authorization checks.

When the web application uses unpredictable IDs but is vulnerable to IDOR, attackers might employ several strategies to discover these IDs:

* Analyzing the logs: when the application logs IDs in a way that can be accessed by users (error messages, audit logs displayed in the GUI)
* Exploiting predictable patterns: when IDs are fully based or partially based on timestamps or have incremental components
* Bruteforcing the IDs
* Monitoring the network traffic
* Exploiting vulnerable endpoints: endpoints that expose object IDs, e.g. through verbose error messages, hidden fields in forms, or URLs 
* Social engineering: manipulating legitimate users into revealing object IDs, through phishing or direct interactions
* Third-party integrations: when third-party services or APIs log or expose the IDs, attackers could target these integrations

## Supporting Evidence

CHANGE ME!

## Recommendation

Ensure that each use of a direct object reference has proper access control checks to verify that a user has permission to access the requested resource.

## Reference

* OWASP Testing Guide (WSTG-ATHZ-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/05-Authorization_Testing/04-Testing_for_Insecure_Direct_Object_References
