# Injection SQL (SQLi)

Sévérité: Majeur  
CVSS: 7.7, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:N/S:C/C:H/I:N/A:N&version=3.1

## Ressources impactées

CHANGE ME!

## Description

Les injections SQL surviennent lorsqu'une application utilise des entrées modifiables par l'utilisateur pour créer des requêtes SQL sans d'abord valider les entrées correctement. Une injection SQL réussie peut lire ou modifier de l'information sensible dans la base de données, exécuter des opérations administratives sur la base de données (ex. la fermer) et même dans certains cas effectuer des commandes sur le serveur.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de bien valider chaque paramètre qui sert à construire les requêtes SQL.

## Références

* Guide de test de l'OWASP (WSTG-INPV-05), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/05-Testing_for_SQL_Injection
* PortSwigger, https://portswigger.net/web-security/sql-injection
