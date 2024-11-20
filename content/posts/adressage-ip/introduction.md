---
title: "Introduction"
summary: Dans ce premier cours, je vous propose de découvrir qu'est ce qu'est l'adressage ip, ses usages etc.
date: 2024-11-19
series: ["Adressage-IP"]
weight: 1
aliases: ["/introduction"]
tags: ["Adressage-IP"]
author: ["Kairrin"]
searchHidden: true
comments: true
cover:
  image: https://raw.githubusercontent.com/Kairrin-net/Kairrin-Website/refs/heads/main/content/posts/adressage-ip/media/introduction.svg
  hidden: true # hide everywhere but not in structured data
  hiddenInList: true # hide on list pages and home
  hiddenInSingle: false # hide on single page
---

> - **Ce premier cours, bien que technique, propose une introduction riche en définitions et exemples pratiques. Si vous souhaitez des     éclaircissements supplémentaires, n’hésitez pas à rejoindre notre [communauté](https://discord.gg/MsAScXtavf).**

---

## Une adresse IP ? Kesako ?

> Une adresse IP (Internet Protocol) est un numéro d'identification unique attribué de façon permanente ou provisoire à chaque périphérique faisant partie d'un même réseau informatique utilisant l'Internet Protocol. 
>
> — <cite>[Wikipedia](https://fr.wikipedia.org/wiki/Adresse_IP)</cite>

En résumé, une adresse IP est un numéro attribué pour pouvoir communiquer avec d'autres appareils qui sont dans le même réseau, ou non.

---

## IPv4, IPv6, quelles différences ? 

#### IPv4

Plus largement utilisée, mais de moins en moins d'adresses disponibles.

Longueur de 32 Bits, soit 4 Octets.

Une adresse IPv4 est exprimée en notation décimale, composée de quatre nombres entiers compris entre 0 et 255, séparés par des points (par exemple : 192.168.0.1).

Environ 4,3 Milliards d'adresses (ou 2^32) pour les connaisseurs 😎.

#### IPv6

Crée principalement pour palier à la pénurie d'IPv4.

Longueur de 128 Bits, soit 16 Octets.

Une adresse IPv6 est exprimée en notation hexadécimale, composée de huit groupes de quatre caractères (chiffres et lettres de A à F), séparés par des doubles points (par exemple : 2001:0db8:85a3:0000:0000:8a2e:0370:7334).

Environ 340 Sextillions d'adresses (*on a le temps avant d'être en rupture..*) ou 2^128.

---

## Les classes d'adresses en IPv4

Chaque adresse IP appartient à une classe, il en existe 5 : A, B, C, D et E. 

| **Classe** | **Plage d'adresses**       | **Bits réservés pour le réseau** | **Nombre d’hôtes**      | **Usage principal**                     |
|------------|-----------------------------|-----------------------------------|--------------------------|------------------------------------------|
| A          | 0.0.0.0 à 126.255.255.255  | 8 bits                           | ~16 millions par réseau | Réseaux très larges (grandes entreprises)|
| B          | 128.0.0.0 à 191.255.255.255| 16 bits                          | ~65 000 par réseau      | Réseaux de taille moyenne               |
| C          | 192.0.0.0 à 223.255.255.255| 24 bits                          | 254 par réseau          | Petits réseaux (ex. : LAN)              |
| D          | 224.0.0.0 à 239.255.255.255| Réservée pour le multicast       | Non applicable          | Transmission de données en groupe       |
| E          | 240.0.0.0 à 255.255.255.255| Réservée pour la recherche       | Non applicable          | Expérimentation                         |

Dans les classes A, B et C il existe ce qu'on appelle des réseaux dit "privés", qui sont réservés à un réseau local (**Exemple : Le réseau interne de votre entreprise, chez vous**). Ces adresses privées ne sont pas utilisables sur internet, car elles ne sont pas routables.

Au contraire, les adresses IP publiques sont routables et utilisées pour permettre la communication entre différents appareils sur Internet. Contrairement aux adresses IP privées ces adresses sont **uniques**.

## Les masques de sous-réseau

#### Format Décimal pointé

Le masque de sous-réseau est représenté par quatre nombres décimaux séparés par des points.

Exemple : 255.255.255.0 

Gardez en tête que chaque masque à son équivalent en CIDR.

#### Format CIDR (Classless InterDomain Routing )

Le masque de sous-réseau est exprimé par le nombre de bits utilisés pour la partie réseau.

Exemple : 255.255.255.0 devient /24, ce qui facilite la compréhension.

Le format CIDR permet de limiter le gaspillage d'adresse et de retarder la pénurie d'adresse IPv4.