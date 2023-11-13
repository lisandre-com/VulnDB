# Cross Site Request Forgery (CSRF)

Sévérité: Modéré  
CVSS: 5.4, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:U/C:L/I:L/A:N&version=3.1

## Ressources impactées

CHANGE ME!

## Description

L'application est vulnérable aux attaques de type Cross Site Request Forgery (CSRF). Cette attaque force un utilisateur à exécuter une action non-intentionnelle dans une application dans laquelle l'utilisateur est présentement authentifié.

À l'aide d’un peu d'ingénierie sociale (comme l'envoi d'un lien malicieux via courriel ou "chat"), un attaquant peut forcer l'utilisateur de l'application web à effectuer une action (au choix de l'attaquant) dans l'application.

Une attaque CSRF réussie peut compromettre les données et opérations lorsqu'elle cible un utilisateur normal. Lorsque la cible est un administrateur de l'application, l'attaque peut compromettre l'application en entier (ex. création de comptes hautement privilégiés pour l'attaquant).

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de protéger TOUTES les fonctionnalités sensibles contre les attaques de type CSRF.

Voir les recommandations : https://cheatsheetseries.owasp.org/cheatsheets/Cross-Site_Request_Forgery_Prevention_Cheat_Sheet.html

## Références

* Guide de test de l'OWASP (WSTG-SESS-05), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/06-Session_Management_Testing/05-Testing_for_Cross_Site_Request_Forgery
* PortSwigger, https://portswigger.net/web-security/csrf
