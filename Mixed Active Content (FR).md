# Combinaison HTTP & HTTPS (_Mixed Active Content_)

Sévérité: Info  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

_Mixed Active Content_ survient lorsqu'une ressource (telle qu'un script ou du CSS) est chargée via HTTP et est incluse dans une page sécurisée (HTTPS). Ceci représente un risque car un attaquant pourrait modifier certains fichiers (alors qu'ils sont non encryptés en transit) – ce qui permet à l'attaquant d'exécuter du code arbitraire (JavaScript ou CSS) dans la page.

Le contenu passif (comme les images) chargé en utilisant une connexion insécure peut également exfiltrer des données ou permettre à l'attaquant de modifier l'apparence de la page (_defacement_), bien qu'il soit moins susceptible de conduire à un compromis complet de l'application.

_Note : Les navigateurs modernes bloquent le contenu HTTP chargé dans les pages sécurisées (HTTPS)._

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé d'accéder uniquement les ressources via HTTPS lorsqu'une application utilise HTTPS (ne pas mélanger des requêtes HTTP et HTTPS dans l'application).

## Références

* Guide de test de l'OWASP (WSTG-CRYP-01), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/09-Testing_for_Weak_Cryptography/01-Testing_for_Weak_Transport_Layer_Security
