# Open Redirection

Sévérité: Mineur  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

Les vulnérabilités de type "Open Redirection" surviennent lorsqu'une application intègre de manière non sécurisée des données contrôlables par l'utilisateur dans la cible d'une redirection. Un attaquant peut construire une URL au sein de l'application qui provoque une redirection vers un domaine externe arbitraire. Ce comportement peut être exploité pour faciliter des attaques d'hameçonnage contre les utilisateurs de l'application. La possibilité d'utiliser une URL d'application authentique, ciblant le domaine correct et avec un certificat SSL valide (si SSL est utilisé), confère de la crédibilité à l'attaque d'hameçonnage, car de nombreux utilisateurs, même s'ils vérifient ces caractéristiques, ne remarqueront pas la redirection ultérieure vers un domaine différent.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de valider les données modifiables par l'utilisateur afin de restreindre les URL autorisées. Idéalement, le parcours d'utilisation de l'application ne devrait pas dépendre de données provenant de sources non fiables.

## Références

* Guide de test de l'OWASP (WSTG-CLNT-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/11-Client-side_Testing/04-Testing_for_Client-side_URL_Redirect
* PortSwigger, https://portswigger.net/web-security/dom-based/open-redirection
