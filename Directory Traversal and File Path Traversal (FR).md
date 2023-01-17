# Directory Traversal / File Path Traversal

Sévérité: Majeur  
CVSS: 7.5, https://nvd.nist.gov/vuln-metrics/cvss/v3-calculator?vector=AV:N/AC:L/PR:N/UI:N/S:U/C:H/I:N/A:N&version=3.1

## Resources impactées

CHANGE ME!

## Description

_Directory Traversal / File Path Traversal_ est une vulnérabilité web qui permet à un attaquant de lire des fichiers arbitraires sur le serveur Web qui exécute l'application. Ceci peut inclure le code et les données de l'application, les noms d'utilisateur et mots de passe pour des systèmes _back-end_, les fichiers de configuration et d'autres fichiers sensibles du système d'exploitation. En tirant parti de ces informations, un attaquant pourrait potentiellement obtenir le contrôle total du serveur - par exemple lorsque le système _back-end_ est accessible à distance avec des informations de connexion trouvées à l'aide de cette vulnérabilité.

_Directory Traversal / File Path Traversal_ est un sous-ensemble de la vulnérabilité web _Local File Inclusion_ (LFI), qui peut lire mais aussi exécuter des fichiers sur le serveur.

## État constaté

CHANGE ME!

## Recommandations

Le moyen le plus efficace d'empêcher les vulnérabilités de type _Directory Traversal / File Path Traversal_ est d'éviter complètement de transmettre l'entrée fournie par l'utilisateur aux API du système de fichiers. De nombreuses fonctions d'application se comportant ainsi peuvent être réécrites pour offrir le même comportement de manière plus sûre.

S'il est jugé inévitable de transmettre les entrées fournies par l'utilisateur aux API du système de fichiers, alors deux mécanismes de défense doivent être utilisées ensemble pour empêcher les attaques :

* L'application doit valider la saisie de l'utilisateur avant de la traiter. Idéalement, la validation doit être comparée à une liste blanche de valeurs autorisées. Si cela n'est pas possible pour la fonctionnalité requise, la validation doit vérifier que l'entrée contient uniquement du contenu autorisé, tel que des caractères purement alphanumériques.

* Après avoir validé l'entrée fournie, l'application doit concaténer l'entrée au répertoire de base et utiliser une API de système de fichiers pour canoniser le chemin. L'API doit vérifier que le chemin canonisé commence par le répertoire de base attendu.

## Références

* https://portswigger.net/web-security/file-path-traversal
* https://owasp.org/www-project-web-security-testing-guide/latest/4-Web_Application_Security_Testing/05-Authorization_Testing/01-Testing_Directory_Traversal_File_Include