---
layout: page
title: Cloud@VD
menu: Cloud
---

{% include link_definitions.md %}

## Services offert

L'infrastructure Cloud@VD offre un service de type Cloud IaaS. Ce service est constitué de plusieurs composants qui
intéragissent entre eux.

* Catalogue d'image système (glance): Ce service offre la possibilité de proposer des images systèmes personnalisées.
Cela permet aux utilisateurs d'avoir à disposition une liste d'application pre-installée sur leurs machines virtuelles.
**Cloud@VD garantie la possibilité de démarrer les images officielles des principales distribution linux (debian, ubuntu,
CentOS), de créer ses propres images mais ne garantie pas le fonctionnement, la disponibilité et l'intégrité des images
créées par les utilisateurs**.

* L'instanciation de machine virtuelle à la demande (nova): Permet de démarrer une machine virtuelle a partir d'une image
du catalogue. Ces machines virtuelles démarrent sur des disques volatiles non sécurisés. Un système de "cache" permet
aux machines virtuelles de démarrer suite à une coupure de courant ou une maintenance sur notre infrastructure.
**Cloud@VD garantie la possibilité de démarrer une machine virtuelle dans la limite des ressources disponibles.
Par contre, nous ne garantissons pas la pérénité des machines virtuelles ni des données qu'elles contiennent.**

* La création de volume persistent (cinder): Ce service permet d'associer à une machine virtuelle un espace de donnée
persistent et résilient. Ce volume doit être vu comme un disque dur externe virtuel. Il peut être attaché ou detaché
d'une machine virtuelle. **Cloud@VD garantie la possibilité de créer des volumes persistent à la demande mais ne garantie
pas la disponibilité ni la sauvegarde des données. Celles-ci sont de la responsabilité des utilisateurs du service Cloud@VD.**