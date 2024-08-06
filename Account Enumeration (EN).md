# Account Enumeration

Severity: Medium  
CVSS: 5.3, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/A:N&version=3.1

## Affected Assets

CHANGE ME!

## Description

An API can be used to enumerate usernames based on the server response. Username enumeration is the first step towards successful brute force attacks (in this system, or others), or password spray attacks (trying a trivial password on a list of usernames).

When an anti-bruteforce mechanism restricts the number of requests sent to the server, the attack can be slowed down, but does not prevent finding valid usernames. The attack can still be automated by adding throttle time between attempts when the list of usernames to try is small.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to display a generic error messages whether the username exists or not. The back-end response must also be generic, i.e the same for valid or invalid usernames.

## Reference

* OWASP Testing Guide (WSTG-IDNT-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/03-Identity_Management_Testing/04-Testing_for_Account_Enumeration_and_Guessable_User_Account
