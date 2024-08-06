# Insecure Direct Object References (IDOR)

Sévérité: Variable  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

Les vulnérabilités de type IDOR (Insecure Direct Object References) surviennent lorsqu'une application fournit un accès direct à des objets en se basant sur des entrées modifiables par l'utilisateur. Ceci permet aux attaquants de contourner l'autorisation et d'accéder directement aux ressources en modifiant la valeur d'un paramètre utilisé pour pointer directement vers un objet.

La cause principale est que l'application prend l'entrée fournie par l'utilisateur et l'utilise pour récupérer un objet sans effectuer de vérifications d'autorisation suffisantes.

Lorsque l'application utilise des identifiants (IDs) imprévisibles mais qu'elle est vulnérable aux attaques IDOR, les attaquants peuvent employer plusieurs stratégies pour découvrir ces identifiants :

* Analyse des logs : lorsque l'application enregistre les IDs d'une manière accessible aux utilisateurs (messages d'erreur, journaux d'audit affichés dans l'interface graphique)
* Exploitation de modèles prévisibles : lorsque les IDs sont entièrement ou partiellement basés sur des horodatages ou ont des composants incrémentiels
* "Bruteforce" des IDs
* Surveillance du trafic réseau
* Exploitation des "endpoints" vulnérables : "endpoints" qui exposent des IDs d'objet, par exemple par le biais de messages d'erreur détaillés, de champs cachés dans les formulaires ou d'URL 
* Ingénierie sociale : manipuler des utilisateurs légitimes pour qu'ils révèlent des IDs d'objets, par hameçonnage ou par des interactions directes
* Intégrations tierces : lorsque des services tiers ou des API enregistrent ou exposent les IDs, les attaquants peuvent cibler ces intégrations

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé de s'assurer que chaque utilisation d'une référence d'objet directe a des contrôles d'accès appropriés pour vérifier qu'un utilisateur a l'autorisation d'accéder à la ressource demandée.

## Références

* Guide de test de l'OWASP (WSTG-ATHZ-04), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/05-Authorization_Testing/04-Testing_for_Insecure_Direct_Object_References
