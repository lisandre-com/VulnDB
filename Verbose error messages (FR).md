# Messages d'erreur divulguant des informations sur l'environnement

Sévérité: Mineur  
CVSS: 3.6, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:L/UI:N/S:U/C:L/I:N/A:N/CR:L/IR:X/AR:X/MAV:X/MAC:X/MPR:X/MUI:X/MS:X/MC:X/MI:X/MA:X&version=3.1

## Ressources impactées

CHANGE ME!

## Description

Selon le contenu des requêtes soumises à l'application, celles-ci peuvent provoquer différentes erreurs.

Certains messages d'erreur contiennent de l'information sur les mécanismes internes techniques qui sont utilisés par la solution et pourraient être considérés comme sensibles puisqu'ils peuvent s'avérer utiles pour un éventuel attaquant.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de ne pas afficher des messages d’erreur trop détaillés techniquement à l'utilisateur ou dans le backend. Configurer le serveur web pour ne pas afficher de messages détaillés.

## Références

* Guide de test de l'OWASP (WSTG-ERRH-01), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/08-Testing_for_Error_Handling/01-Testing_For_Improper_Error_Handling
