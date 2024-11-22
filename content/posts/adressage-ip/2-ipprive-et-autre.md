---
title: "2 : Les adresses IP privées et cas particuliers"
summary: Ce cours explore l’importance et les applications des adresses IP privées, ainsi que des adresses spéciales comme les adresses loopback et APIPA. Vous apprendrez à distinguer leurs usages.
date: 2024-11-22
series: ["Adressage-IP"]
weight: 2
aliases: ["/ipprive-et-autre"]
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

#### 🫣 Pourquoi les appeler privée ?

Car ces adresses ne peuvent pas recevoir de trafic de l’extérieur directement. Pour pouvoir communiquer avec Internet, elles passent par un routeur [NAT](https://www.fortinet.com/fr/resources/cyberglossary/network-address-translation#:~:text=Définition%20de%20la%20traduction%20d,une%20seule%20adresse%20IP%20publique.), qui permet à tout un réseau d’avoir une seule adresse IP publique. Nous reviendrons sur le NAT dans un prochain cours.

---

#### 📚 Les différentes adresses privées

| **Classe**  | **Plage d'adresses privées**      | **Masque de sous réseau** | 
|---------|-------------------------------|--------------------------------|
| Classe A | 10.0.0.0 à 10.255.255.255    | 255.0.0.0            
| Classe B | 172.16.0.0 à 172.31.255.255  | 255.255.O.0                   
| Classe C | 192.168.0.0 à 192.168.255.255| 255.255.255.0                      

Par exemple, votre box utilise sûrement les adresses IP privées de classe C.

#### ❓ Les exceptions

Il existe plusieurs adresses, qui ont un usage bien particulier, les voici :

- **0.0.0.0** [ROUTE PAR DÉFAUT](http://cisco.ofppt.info/ccna2/course/module6/6.2.2.1/6.2.2.1.html#:~:text=Une%20route%20par%20défaut%20est%20utilisée%20lorsqu'aucune%20autre%20route,comme%20passerelle%20de%20dernier%20recours.) : Elle permet d'indiquer une route par défaut sur un routeur.

- **169.254.0.0/16** [APIPA](https://forum.huawei.com/enterprise/fr/adresse-apipa-qu-est-ce-que-c-est/thread/667502567447478272-667481000260808704) : Ce réseau est automatiquement paramétré sur votre poste quand la rêquete vers le serveur DHCP à échoué.

- **127.0.0.1** [LOOPBACK](https://fr.wikipedia.org/wiki/Loopback) : L'adresse de loopback représente la machine, elle permet aussi de se connecter à un serveur web auto-hébergé sur le poste. 

## 👍 Pour aller plus loin

[Exercices sur l'adressage IPv4 **inetdoc.net**](https://www.inetdoc.net/articles/adressage.ipv4/adressage.ipv4.exercises.html)

[Exercices d’adressage IP **ofppt.info**](https://ofppt.info/exercices-dadressage-ip/)

[Les classes d'adresses : **inetdoc.net**](https://www.inetdoc.net/articles/adressage.ipv4/adressage.ipv4.class.html)

[Les adresses IP pour les débutants : **IT-Connect.fr**](https://www.it-connect.fr/les-adresses-ip-pour-les-debutants/#III_Adresses_IPv4_et_IPv6)

[Adresses IP publiques et privées : quelle est la différence - **Avast.com**](https://www.avast.com/fr-fr/c-ip-address-public-vs-private)


## ℹ️ Sources

[Classe d'adresse IP : **Wikipedia.org**](https://fr.wikipedia.org/wiki/Classe_d%27adresse_IP)

[Adresse IP : **Wikipedia.org**](https://fr.wikipedia.org/wiki/Adresse_IP)


**Merci à tous d'avoir lu cet article, à bientôt !**

