# Buffer Overflow

Severity: Critical  
CVSS: 10.0, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H&version=3.1

## Affected Assets

CHANGE ME!

## Description

A buffer overflow, or buffer overrun, is an anomaly where a program, while writing data to a buffer, overruns the buffer's boundary and overwrites adjacent memory locations.

Buffers are areas of memory set aside to hold data, often while moving it from one section of a program to another, or between programs. Buffer overflows can often be triggered by malformed inputs; if one assumes all inputs will be smaller than a certain size and the buffer is created to be that size, then an anomalous transaction that produces more data could cause it to write past the end of the buffer. If this overwrites adjacent data or executable code, this may result in erratic program behavior, including memory access errors, incorrect results, and crashes.

By sending in data designed to cause a buffer overflow, it is possible to write into areas known to hold executable code and replace it with malicious code, or to selectively overwrite data pertaining to the program's state, therefore causing behavior that was not intended by the original programmer.

## Supporting Evidence

CHANGE ME!

## Recommendation

If a security patch for the buffer overflow vulnerability exists for the affected component, apply it as soon as possible.

For custom code development, review all code that accepts input from users and ensure that it provides appropriate size checking on all such inputs. This should be done even for environments that are not susceptible to such attacks as overly large inputs that are uncaught may still cause denial of service or other operational problems.

## Reference

* OWASP Testing Guide (WSTG-INPV-13), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/13-Testing_for_Format_String_Injection
* OWASP, https://owasp.org/www-community/vulnerabilities/Buffer_Overflow
* Wikipedia, https://en.wikipedia.org/wiki/Buffer_overflow
