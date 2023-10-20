# Librairies contenant des vulnérabilités connues

Sévérité: Variable  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

L'utilisation de librairies JavaScript tierces peut introduire diverses vulnérabilités. Les librairies JavaScript couramment utilisées bénéficient généralement d'un audit approfondi. Cela signifie que les bogues sont rapidement identifiés et corrigés en amont, ce qui entraîne un flux constant de mises à jour de sécurité à appliquer. Bien qu'il puisse être tentant d'ignorer ces correctifs de sécurité, l'utilisation d'une librairie non à jour peut rendre une application web extrêmement vulnérable aux attaques. Il est donc important de s'assurer que toutes les mises à jour de sécurité disponibles sont appliquées rapidement.

Certaines vulnérabilités exposent chaque application qui importe la librairie, tandis que d'autres n'affectent que les applications utilisant certaines fonctionnalités de la librairie. Identifier avec précision quelles vulnérabilités d'une librairie s'appliquent à cette application web spécifique peut être difficile et prendre beaucoup de temps dans le cadre d'un test d'intrusion. Par conséquent, il est recommandé d'appliquer toutes les mises à jour de sécurité disponibles, quel que soit le cas.

## État constaté

CHANGE ME!

## Recommandations

Il est recommandé d'élaborer une stratégie de gestion des correctifs pour s'assurer que les mises à jour de sécurité sont appliquées rapidement à toutes les librairies tierces de l'application. De plus, il est préférable de réduire la surface d'attaque en supprimant les librairies qui ne sont plus utilisées.

## Références

* https://owasp.org/www-project-top-ten/2017/A9_2017-Using_Components_with_Known_Vulnerabilities
* https://cwe.mitre.org/data/definitions/1104.html
