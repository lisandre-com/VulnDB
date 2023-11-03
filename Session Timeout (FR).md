# Délai d'expiration de session

Sévérité: Mineur  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

Les applications web devraient limiter la durée de la session après une période d'inactivité. Ce délai d'expiration correspond à la durée pendant laquelle une session restera active en l'absence d'activité de l'utilisateur, fermant et invalidant la session après la période d'inactivité définie depuis la dernière requête HTTP reçue par l'application web pour un identifiant de session donné. Le délai d'expiration de session le plus approprié devrait être un équilibre entre la sécurité (temps d'inactivité plus court) et la convivialité (temps d'inactivité plus long), et dépend fortement du niveau de sensibilité des données manipulées par l'application.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de fixer une durée de session appropriée en fonction des données stockées ou traitées par l'application. Les délais d'expiration de session typiques varient de 15 à 60 minutes.

## Références

* Guide de test de l'OWASP (WSTG-SESS-07), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/06-Session_Management_Testing/07-Testing_Session_Timeout
