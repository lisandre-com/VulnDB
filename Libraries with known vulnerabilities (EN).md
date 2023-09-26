# Libraries with known vulnerabilities

Severity: Varies
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

The use of third-party JavaScript libraries can introduce a range of vulnerabilities. Common JavaScript libraries typically have the benefit of being heavily audited. This may mean that bugs are quickly identified and patched upstream, resulting in a steady stream of security updates that need to be applied. Although it may be tempting to ignore updates, using a library with missing security patches can make a web application exceptionally easy to exploit. Therefore, it's important to ensure that any available security updates are applied promptly.

Some library vulnerabilities expose every application that imports the library, but others only affect applications that use certain library features. Accurately identifying which library vulnerabilities apply to this specific web application can be difficult and time-consuming, so it is recommended to apply all available security updates regardless.

## Supporting Evidence

CHANGE ME!

## Recommendation

Develop a patch-management strategy to ensure that security updates are promptly applied to all third-party libraries in your application. Also, consider reducing your attack surface by removing any libraries that are no longer in use.

## Reference

* https://owasp.org/www-project-top-ten/2017/A9_2017-Using_Components_with_Known_Vulnerabilities
* https://cwe.mitre.org/data/definitions/1104.html
