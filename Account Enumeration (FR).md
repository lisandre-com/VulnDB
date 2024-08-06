# Énumération des noms d'utilisateur

Sévérité: Modéré  
CVSS: 5.3, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:U/C:L/I:N/A:N&version=3.1

## Ressources impactées

CHANGE ME!

## Description

Une API peut être utilisée pour énumérer les noms d'utilisateur valides en se basant sur les réponses du serveur. L'énumération de noms d'utilisateur est la première étape menant à une attaque de type "bruteforce" réussie (dans ce système ou dans un autre), ou d'une attaque de type "password spray" (essayer un mot de passe trivial sur une liste de noms d'utilisateur).

Lorsqu'un mécanisme "anti-bruteforce" restreint le nombre de requêtes envoyées au serveur, l'attaque peut être ralentie, mais ceci ne prévient pas l'obtention de noms d'utilisateur valides. L'attaque peut tout de même être automatisée en ajoutant un délai entre les essais lorsque la liste de noms d'utilisateur à essayer est courte.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé d'afficher le même message générique lorsqu'un utilisateur est valide ou non. La réponse du "back-end" doit également être générique, c'est-à-dire la même pour un utilisateur valide ou non.

## Références

* Guide de test de l'OWASP (WSTG-IDNT-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/03-Identity_Management_Testing/04-Testing_for_Account_Enumeration_and_Guessable_User_Account
