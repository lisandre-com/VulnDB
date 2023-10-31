# Session Timeout

Severity: Low  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

Web applications should implement an idle or inactivity timeout for sessions. This timeout defines the amount of time a session will remain active in case there is no activity by the user, closing and invalidating the session upon the defined idle period since the last HTTP request received by the web application for a given session ID. The most appropriate timeout should be a balance between security (shorter timeout) and usability (longer timeout) and heavily depends on the sensitivity level of the data handled by the application.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to fix a session duration appropriate in relation to the data stored/processed by the application. Typical session expiration vary from 15 to 60 minutes.

## Reference

* OWASP Testing Guide (WSTG-SESS-07), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/06-Session_Management_Testing/07-Testing_Session_Timeout
