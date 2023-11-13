# Clickjacking (UI redressing)

Sévérité: Modéré  
CVSS: 6.1, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:R/S:C/C:L/I:L/A:N

## Ressources impactées

CHANGE ME!

## Description

L'application est vulnérable aux attaques de type clickjacking. Le détournement de clic ou clickjacking consiste à utiliser les propriétés HTML d'une page Web pour manipuler son affichage, en superposant une couche transparente à la page visible, afin de tromper l'utilisateur qui, en cliquant sur un lien ou un bouton en apparence inoffensif, exécute des actions, sans s'en apercevoir, sur la page dissimulée.

Le détournement de clic peut notamment servir à obtenir les informations de connexion de l'utilisateur en combinaison avec une attaque d'hameçonnage.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de prévenir l'inclusion de l'application dans les balises "iframe" à l'aide du mécanisme de Content Security Policy (CSP) et de la directive frame-ancestors dans les réponses du serveur. Ceci remplace l'ancienne option "X-Frame-Options: sameorigin" selon l'OWASP.

## Références

* Guide de test de l'OWASP (WSTG-CLNT-09), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/09-Testing_for_Clickjacking
* PortSwigger, https://portswigger.net/web-security/clickjacking
