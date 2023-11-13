# Cross Site Scripting (XSS)

Sévérité: Modéré  
CVSS: 4.6, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:R/S:U/C:L/I:L/A:N&version=3.1

## Ressources impactées

CHANGE ME!

## Description

L'application web est vulnérable aux attaques de type Cross site scripting (XSS), qui permettent à un attaquant d'injecter des scripts (côté client) dans des pages web visitées par d'autres utilisateurs.

Cette vulnérabilité survient lorsque la validation des entrées n'est pas faite correctement. Le contenu malicieux apparait donc comme faisant partie de l'application web et s'exécute dans le navigateur de l'utilisateur avec les permissions de l'application web.

Cette vulnérabilité peut être exploitée pour mener diverses attaques sur le navigateur, incluant :

* Vol de session
* Obtention d'informations sensibles accédées par les utilisateurs de l'application
* Dégradation ("defacement") de l'application
* Balayage de ports des serveurs internes ("internes" par rapport à l'utilisateur de l'application)
* Déploiement d'exploits du navigateur
* Autres activités malicieuses


## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de toujours valider les entrées. NE JAMAIS faire confiance aux entrées de l'utilisateur.

Voir les recommandations :  https://en.wikipedia.org/wiki/Cross-site_scripting#Preventive_measures

## Références

* Guide de test de l'OWASP (WSTG-INPV-01), reflected XSS, https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/01-Testing_for_Reflected_Cross_Site_Scripting
* Guide de test de l'OWASP (WSTG-INPV-02), stored XSS, https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/02-Testing_for_Stored_Cross_Site_Scripting
* Guide de test de l'OWASP (WSTG-CLNT-01), DOM-based XSS, https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/01-Testing_for_DOM-based_Cross_Site_Scripting
* PortSwigger, https://portswigger.net/web-security/cross-site-scripting
