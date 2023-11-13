# Buffer Overflow

Sévérité: Critique  
CVSS: 10.0, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:C/C:H/I:H/A:H&version=3.1

## Ressources impactées

CHANGE ME!

## Description

Un buffer overflow, ou buffer overrun, est une anomalie dans laquelle un programme, tout en écrivant des données dans une mémoire tampon (buffer), dépasse la limite de la mémoire tampon et écrase les emplacements de mémoire adjacents.

Les tampons sont des zones de mémoire réservées pour contenir des données, souvent lors de leur déplacement d'une section d'un programme à une autre, ou entre des programmes. Les buffer overflows peuvent souvent être déclenchés par des entrées mal formées ; si l'on suppose que toutes les entrées seront inférieures à une certaine taille et que le tampon est créé pour avoir cette taille, alors une transaction anormale produisant plus de données pourrait l'amener à écrire au-delà de la fin du tampon. Si cela écrase les données adjacentes ou le code exécutable, cela peut entraîner un comportement erratique du programme, notamment des erreurs d'accès à la mémoire, des résultats incorrects et l'arrêt du programme.

En envoyant des données conçues pour provoquer un buffer overflow, il est possible d'écrire dans des zones connues pour contenir du code exécutable et de le remplacer par un code malveillant, ou d'écraser de manière sélective les données relatives à l'état du programme, provoquant ainsi un comportement qui n'était pas prévu par le programmeur d'origine.

## État constaté

CHANGE ME!

## Recommandations

Si un correctif de sécurité pour la vulnérabilité de buffer overflow existe pour le composant affecté, appliquez-le dès que possible.

Pour le développement de code personnalisé, examinez tout le code qui accepte les entrées des utilisateurs et assurez-vous qu'il fournit une vérification de taille appropriée sur toutes ces entrées. Cela doit être fait même pour les environnements qui ne sont pas sensibles à de telles attaques, car des entrées trop volumineuses qui ne sont pas interceptées peuvent toujours provoquer un déni de service ou d'autres problèmes opérationnels.

## Références

* Guide de test de l'OWASP (WSTG-INPV-13), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/07-Input_Validation_Testing/13-Testing_for_Format_String_Injection
* OWASP, https://owasp.org/www-community/vulnerabilities/Buffer_Overflow
* Wikipedia, https://en.wikipedia.org/wiki/Buffer_overflow
