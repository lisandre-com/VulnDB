# SQL Injection (SQLi)

Severity: High  
CVSS: 7.7, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:N/S:C/C:H/I:N/A:N&version=3.1

## Affected Assets

CHANGE ME!

## Description

SQL injections happen when an application uses user-controlled input to create SQL queries without properly validating the input first. A successful SQL injection attack can read or modify sensitive data from the database, execute administration operations on the database (e.g. shutdown), and in some cases issue commands on the operating system.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to validate all inputs that are used to build SQL queries.

## Reference

* OWASP Testing Guide (WSTG-INPV-05), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/05-Testing_for_SQL_Injection
* PortSwigger, https://portswigger.net/web-security/sql-injection
