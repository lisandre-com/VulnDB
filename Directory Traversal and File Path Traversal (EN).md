# Directory Traversal / File Path Traversal

Severity: High  
CVSS: 7.5, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N&version=3.1

## Affected Assets

CHANGE ME!

## Description

Directory Traversal / File Path Traversal is a web security vulnerability that allows an attacker to read arbitrary files on the web server that is running the application. This might include application code and data, credentials for back-end systems, configuration files, and other sensitive operating system files. Leveraging this information, an attacker could potentially gain full control of the server - for example when the backend system is remotely accessible with credentials found using this vulnerability.

Directory Traversal / File Path Traversal is a subset of the web security vulnerability Local File Inclusion (LFI), which can read but also execute files on the server.

## Supporting Evidence

CHANGE ME!

## Recommendation

The most effective way to prevent file path traversal vulnerabilities is to avoid passing user-supplied input to filesystem APIs altogether. Many application functions that do this can be rewritten to deliver the same behavior in a safer way.
If it is considered unavoidable to pass user-supplied input to filesystem APIs, then two layers of defense should be used together to prevent attacks:

* The application should validate the user input before processing it. Ideally, the validation should compare against a whitelist of permitted values. If that isn't possible for the required functionality, then the validation should verify that the input contains only permitted content, such as purely alphanumeric characters.

* After validating the supplied input, the application should append the input to the base directory and use a platform filesystem API to canonicalize the path. It should verify that the canonicalized path starts with the expected base directory.

## Reference

* https://portswigger.net/web-security/file-path-traversal
* OWASP Testing Guide (WSTG-ATHZ-01), https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/05-Authorization_Testing/01-Testing_Directory_Traversal_File_Include
