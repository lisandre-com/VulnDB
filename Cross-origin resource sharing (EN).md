# Cross-origin resource sharing (CORS)

Severity: High (varies based on information obtained)  
CVSS: 7.1, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:U/C:H/I:L/A:N&version=3.1  
(Integrity can be impacted depending on information obtained by APIs, like session IDs, keys, tokens, etc.)

## Affected Assets

CHANGE ME!

## Description

An HTML5 cross-origin resource sharing (CORS) policy controls whether and how content running on other domains can perform two-way interaction with the domain that publishes the policy. The policy is fine-grained and can apply access controls per-request based on the URL and other features of the
request.

Trusting arbitrary origins effectively disables the same-origin policy, allowing two-way interaction by third-party web sites. Unless the response consists only of unprotected public content, this policy is likely to present a security risk.

If the site specifies the header "Access-Control-Allow-Credentials: true", third-party sites may be able to carry out privileged actions and retrieve sensitive information. Even if it does not, attackers may be able to bypass any IP-based access controls by proxying through users' browsers.

## Supporting Evidence

CHANGE ME!

## Recommendation

It is recommended to review the configuration of CORS for the impacted resource(s). Use a whitelist of trusted domains.

## Reference

* OWASP Testing Guide (WSTG-CLNT-07), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/07-Testing_Cross_Origin_Resource_Sharing
* PortSwigger, https://portswigger.net/web-security/cors
