# DLL Hijacking

Sévérité: Variable  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

L’attaque "**DLL Search Order Hijacking**" exploite la manière dont Windows résout les DLLs lorsque l'application ne définit pas explicitement le chemin complet. L'application XYZ est vulnérable à cette attaque. Le dossier applicatif de XYZ (C:\Program Files\XYZ) vient avant C:\Windows\System32 dans l'ordre de la recherche du fichier DLL. Placer un fichier DLL malicieux dans le dossier applicatif de XYZ résulte donc en l'éxécution du fichier DLL malicieux.

L'attaque "**Relative Path DLL Hijacking**" est une variante de l'attaque "DLL Search Order Hijacking". L'attaquant écrit (et renomme généralement) un fichier exécutable légitime, accompagné de sa DLL malveillante, dans un dossier autorisé à y accéder. Cette technique nécessite un exécutable légitime qui ne spécifie pas de chemin absolu pour les fichiers DLL. Si aucun chemin absolu n'est spécifié, Windows recherche le fichier DLL selon l'ordre de recherche prédéfini. L'application XYZ est vulnérable à cette attaque. Copier le fichier exécutable dans un autre dossier et y placer un fichier DLL malicieux résulte en l’exécution du fichier DLL malicieux.

## État constaté

CHANGE ME!

## Recommandations

* Les développeurs devraient exiger des chemins d'accès définis pour les DLL dans les applications.
* Lorsque possible, inclure des valeurs de hachage dans les fichiers de manifest afin d'empêcher le "side-loading" de librairies malicieuses.
* Interdire le chargement de DLL distantes. Cette option est incluse par défaut dans Windows Server 2012+ et est disponible via un correctif pour XP+ et Server 2003+.
* Activer le "Safe DLL Search Mode" pour déplacer le dossier actuel de l'utilisateur plus loin dans l'ordre de recherche des DLLs. Cette option est incluse par défaut dans les versions modernes de Windows; la clé de registre Windows associée est HKLM\SYSTEM\CurrentControlSet\Control\Session Manager\SafeDLLSearchMode.
* Mettre régulièrement à jour les logiciels pour inclure les correctifs corrigeant les vulnérabilités liées aux DLLs.

## Références

* Hijack Execution Flow: DLL (T1574.001), https://attack.mitre.org/techniques/T1574/001/
