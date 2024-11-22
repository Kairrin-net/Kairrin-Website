---
title: "2 : Les adresses IP privées et cas particuliers"
summary: Ce cours explore l’importance et les applications des adresses IP privées et publiques à travers plusieurs exemples concrets. Vous apprendrez à distinguer leurs usages, leurs avantages, ainsi que leurs rôles respectifs dans les réseaux locaux et Internet.
date: 2024-11-22
series: ["Adressage-IP"]
weight: 2
aliases: ["/2-ipprive-et-autre"]
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

## Ce qu'on à vu précédemment

> - Dans la première partie du cours, nous avons abordé les différentes adresses IP, notamment les privées et les publiques. Dans cette partie, je vais vous expliquer l’intérêt des adresses IP privées ainsi que celui de certaines adresses IP un peu particulières.

---

## Les IP privées

#### Utilité

Dans un [LAN](https://www.cloudflare.com/fr-fr/learning/network-layer/what-is-a-lan/), les adresses IP privées occupent une place essentielle dans toute infrastructure. Sans ces adresses, vous ne pourriez pas communiquer avec votre serveur de fichiers ou même accéder au reste d’Internet (le [WAN](https://www.cloudflare.com/fr-fr/learning/network-layer/what-is-a-wan/)).

#### Pourquoi les appeler privée ?

Car ces adresses ne peuvent pas recevoir de trafic de l’extérieur directement. Pour pouvoir communiquer avec Internet, elles passent par un routeur [NAT](https://www.fortinet.com/fr/resources/cyberglossary/network-address-translation#:~:text=Définition%20de%20la%20traduction%20d,une%20seule%20adresse%20IP%20publique.), qui permet à tout un réseau d’avoir une seule adresse IP publique. Nous reviendrons sur le NAT dans un prochain cours.

---

