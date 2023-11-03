# Information sensible divulguée (version du serveur web)

Sévérité: Info  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

Le serveur web révèle des informations précises sur sa version. Ces informations peuvent aider un attaquant à exploiter d'autres vulnérabilités existantes. L'attaquant peut chercher les vulnérabilités spécifiques à la version utilisée et les exploiter si le serveur n'a pas les correctifs en place.

## État constaté

CHANGE ME!

## Recommandations

Bien que les informations de serveur exposées ne soient pas nécessairement en soi une vulnérabilité, ce sont des informations qui peuvent aider les attaquants à exploiter d'autres vulnérabilités qui peuvent exister. Les informations de serveur exposées peuvent également amener les attaquants à trouver des vulnérabilités de serveur spécifiques à la version qui peuvent être utilisées pour exploiter des serveurs non mis à jour. Pour cette raison, il est recommandé de prendre certaines précautions. Ces mesures comprennent :

* La suppression des informations du serveur Web des en-têtes HTTP, comme avec le module mod_headers d'Apache.

* L'utilisation d'un serveur proxy inverse ("reverse proxy") pour créer une couche de sécurité supplémentaire entre le serveur Web et Internet.

* S'assurer que les serveurs Web sont mis à jour avec les derniers logiciels et correctifs de sécurité.

## Références

* Guide de test de l'OWASP (WSTG-INFO-02), https://owasp.org/www-project-web-security-testing-guide/stable/4-Web_Application_Security_Testing/01-Information_Gathering/02-Fingerprint_Web_Server
