# Non-production environments

Severity: Low  
CVSS: N/A

## Affected Assets

CHANGE ME!

## Description

**Non-production environments exposed on the internet:**
Search of subdomains found non-production environment(s) exposed on the internet. Non-production environments might be interesting for a potential attacker since they might have weaker security controls (e.g. less monitoring, weaker authentication methods, no anti-bruteforce mechanisms, new features containing new vulnerabilities, etc.) and often contain a subset of production data. When it comes to security, the focus is typically on the production environment because it contains the "real" data. Access to these environments should be restricted to appropriate companies and people.

**Incomplete segmentation between production and non-production environments:**
The non-production environment is not completely isolated from the production environment. The non-production environment sometimes calls URLs/APIs from production. A bad segmentation between production and non-production environments can cause problems on production systems (mostly on confidentiality and integrity but could also slow down production network).

**Production data in non-production environments:**
When production data is used in non-production environments, it is required to be protected at the same level than the production environment, which can add significantly to the time and expense of testing the system. When it is not possible to use test data, production data should be masked / anonymized.

## Supporting Evidence

CHANGE ME!

## Recommendation

* **Non-production environments exposed on the internet:**
It is recommended to restrict access to non-production environments to appropriate people by using a whitelist of IPs that must access it.

* **Incomplete segmentation between production and non-production environments:**
It is recommended to completely isolate production from non-production environments. Verify all links (URLs) in non-production environments and API calls.

* **Production data in non-production environments:**
It is recommended to generate test data instead of using production data. When it is not possible to use test data, production data should be masked / anonymized.

## Reference

N/A
