# Environnements de non-production

Sévérité: Mineur  
CVSS: N/A

## Ressources impactées

CHANGE ME!

## Description

**Environnements de non-production exposés sur internet :**
La recherche de sous-domaines a révélé des environnements de non-production exposés sur internet. Les environnements de non-production peuvent être intéressants pour un attaquant potentiel car les contrôles de sécurité sont souvent moins robustes (ex. : moins de surveillance, des méthodes d'authentification plus faibles, aucun mécanisme "anti-bruteforce", de nouvelles fonctionnalités contenant de nouvelles vulnérabilités, etc.) et contiennent souvent un sous-ensemble des données de production. En matière de sécurité, l'accent est généralement mis sur l'environnement de production car il contient les données "réelles". L'accès à ces environnements devrait être restreint aux compagnies et personnes concernées.

**Segmentation incomplète entre les environnements de production et non-production :**
L'environnement de non-production n'est pas complètement isolé de la production. L'environnement appelle parfois des URLs/APIs de production. Une mauvaise séparation entre les environnements de production et non-production peut causer des problèmes sur les systèmes de production (entres autres avec les outils automatisés qui suivent les liens).

**Données de production dans les environnements de non-production :**
Lorsque des données de production sont utilisées dans des environnements de non-production, elles doivent être protégées au même niveau que l'environnement de production, ce qui peut augmenter considérablement le temps et les dépenses liés aux tests du système. Lorsqu'il n'est pas possible d'utiliser des données de test, les données de production doivent être masquées / anonymisées.

## État constaté

CHANGE ME!

## Recommandations

* **Environnements de non-production exposés sur internet :**
Il est recommandé de restreindre l'accès aux environnements de non-production aux compagnies et personnes concernées à l'aide d'une "whitelist" des adresses IP qui doivent y accéder.

* **Segmentation incomplète entre les environnements de production et non-production :**
Il est recommandé de séparer complètement les environnements de non-production de ceux de production. Vérifier tous les liens (URLs) en non-production et les appels d'API.

* **Données de production dans les environnements de non-production :**
Il est recommandé de générer des données de test plutôt que d'utiliser des données de production. Lorsqu'il n'est pas possible d'utiliser des données de test, les données de production doivent être masquées / anonymisées.

## Références

N/A
