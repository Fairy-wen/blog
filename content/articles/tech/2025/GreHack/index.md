+++
title = "GreHack 2025"
date = 2026-01-13
tags = ["conference", "sketchnotes"]
categories = ["tech"]
+++

Dernière conférence à laquelle je me rends cette année, le [GreHack](https://grehack.fr/) : conférence grenobloise axée sur la cybersécurité.  
J'y ai assisté avec quelques collègues de [Quarkslab](https://www.quarkslab.com/), dont Rayan qui y animait un workshop.  
L'idée pour moi était d'en découvrir un peu plus sur le monde de la cybersécurité d'un point de vue attaquant.  

Plusieurs thématiques au rendez-vous : compromission de matériel, dump de base de fichiers, tests d'intrusion physique dans un bâtiment, rétro-ingénierie logicielle, failles réseau... Il y en a pour tous les profils.  

Ici il n'y a qu'une "track", comprenez une seule salle et donc un seul talk à la fois durant la journée du vendredi.  
Puis le soir (18h00-21h00), les différents workshops prennent place et enfin le samedi tout le monde peut s'affronter en équipes au cours d'un [CFT](https://grehack.fr/ctf/) (Capture The Flag) lors duquel il faudra parvenir à relever différents défis et marquer le plus de points pour gagner un bouteille de Chartreuse.  
Pour ma part cette année je n'ai pu assister qu'aux conférences de la journée de vendredi, ce qui a tout de même été très intéressant et enrichissant.  

_Détail qui a son importance, toutes les conférences sont en anglais, double dose de travail pour le cerveau !_

## CTF in a box ? The weirdest NETGEAR network switch 2021 exploit chain
[Gynvael Coldwind](https://gynvael.coldwind.pl/)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=ecf2-EJIKnXn0NHv&t=504)  

Cette première présentation pourrait faire office de keynote en conférence, tant elle a été bien menée et dont le sujet est un bel exemple de la recherche de vulnérabilités sur un équipement (ici, un équipement réseau).  

Créativité, diversité des champs d'attaque, un cas d'école qu'il faudrait montrer aux équipes de dev pour leur découvrir ce que sont réellement les failles de sécurité, comment elles sont découvertes et exploitées.

![CTF in a box, Sketchnote 1 sur 5](img/GreHack%202025_1.png "CTF in a box, Sketchnote 1 sur 5")  
![CTF in a box, Sketchnote 2 sur 5](img/GreHack%202025_2.png "CTF in a box, Sketchnote 2 sur 5")  
![CTF in a box, Sketchnote 3 sur 5](img/GreHack%202025_3.png "CTF in a box, Sketchnote 3 sur 5")  
![CTF in a box, Sketchnote 4 sur 5](img/GreHack%202025_4.png "CTF in a box, Sketchnote 4 sur 5")  
![CTF in a box, Sketchnote 5 sur 5](img/GreHack%202025_5.png "CTF in a box, Sketchnote 5 sur 5")  

## Adobe and SAP: All Your Business Documents Belong To Us
[Yvan Genuer](https://www.linkedin.com/in/1ggy/) and [Fabian Hagg](https://www.linkedin.com/in/fabian-hagg-015b00190/)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=D77ZUBLZRATnRVnU&t=3783)  

Le deuxième sujet traite de la sécurité d'une infrastructure Adobe Document Services (Adobe + SAP), dont l'analyse des requêtes client-serveur a permis de réaliser d'une part de une attaque type [Man-in-the-middle](https://fr.wikipedia.org/wiki/Attaque_de_l%27homme_du_milieu) et une compromission de fichiers, et d'autre part une exécution de code à distance.  

Cette présentation a notamment montré comment un protocole de communication propriétaire peut être décortiqué afin de le transformer en vecteur d'attaque.  
Et en conclusion : toujours appliquer les mises à jour de sécurité qui justement corrigent ce type de vulnérabilités...


![Adobe and SAP, Sketchnote 1 sur 3](img/GreHack%202025_6.png "Adobe and SAP, Sketchnote 1 sur 3")  
![Adobe and SAP, Sketchnote 2 sur 3](img/GreHack%202025_7.png "Adobe and SAP, Sketchnote 2 sur 3")  
![Adobe and SAP, Sketchnote 3 sur 3](img/GreHack%202025_8.png "Adobe and SAP, Sketchnote 3 sur 3")  


## One does not simply walk into a building... or do they?
[Volker Carstein](https://github.com/volker-carstein)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=v9dHFVrQPj4yzLxZ&t=7941)  

Ce talk est un retour d'expérience sur une campagne d'audit d'intrusion physique au sein des locaux de l'entreprise mandataire, avec quelques défis supplémentaires à relever tels que le vol d'informations confidentielles, le vol de matériel ou encore la compromission de l'infra réseau.  
Ce genre de mission requiert une combinaison de compétences et une multitudes d'étapes afin d'être menée à bien, avec notamment du repérage en amont (des locaux, des codes vestimentaires, des habitudes des employés, des services tiers comme le ménage, le gardiennage, les livraisons de colis...), des compétence en crochetage de serrures, du [social engineering](https://fr.wikipedia.org/wiki/Ing%C3%A9nierie_sociale_(s%C3%A9curit%C3%A9_de_l%27information)), de l'[OSINT](https://fr.wikipedia.org/wiki/Renseignement_d%27origine_sources_ouvertes) et j'en passe.  

Je n'ai pas pris de sketchnotes sur ce sujet, je vous recommande vivement de regarder la vidéo (elle vaut le détour) !

## Abstractions for Program Analysis
[Kyle Martin](https://github.com/ElykDeer)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=O9COXsEC1hQ0YAui&t=9760)  

Kyle vient nous présenter le principe de l'abstraction pour l'analyse de programmes, notamment de binaires.  
En effet, il est possible de décompiler des exécutables pour tenter d'en retrouver le code source, ou au moins comprendre ce que fait le programme en question.  

Les décompilateurs peuvent donc faire à appel à de l'abstraction pour tenter de reconstituer le puzzle de départ.  
Je n'ai pas pris de sketchnotes, et suis bien incapable de restituer le contenu du talk ici, donc je vous invite à aller regarder la vidéo.  
Le sujet est vraiment intéressant pour prendre un peu de hauteur sur la programmation en général, et l'analyse de binaires.  

## Smart Charger, Dumb Idea?
[Aymeric Palhière](https://www.linkedin.com/in/aymeric-palhi%C3%A8re-b19ba313b/)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=4LxIsjip7d0rsMgK&t=11892)  

La journée se poursuit avec la présentation d'Aymeric qui a éprouvé la sécurité des chargeurs intelligents de voitures électriques, et nous présente quelques failles observées.  

Ce type d'équipement commence à être régulièrement présent sur les challenge Pwn2Own (compétitions lors desquelles des équipes s'affrontent pour trouver et exploiter des failles sur des équipements, et inciter les fabricants à améliorer la sécurité de ces derniers).  
La fatigue commençant à pointer le bout de son nez, j'ai principalement pris des notes sur le contexte, mais pas sur le détail des vulnérabilités.  

TL;DR : Aymeric est parvenu à exécuter du code sur le chargeur.  

![Smart car-chargers, Sketchnote 1 sur 2](img/GreHack%202025_9.png "Smart car-chargers, Sketchnote 1 sur 2")  
![Smart car-chargers, Sketchnote 2 sur 2](img/GreHack%202025_10.png "Smart car-chargers, Sketchnote 2 sur 2")  


## Exploring Browser Permissions and Exploiting Permission Hijacking
[Alberto Fernandez-de-Retana _aka Bubu_](https://albertofdr.github.io/)  

[Captation](https://www.youtube.com/live/F4CudbWHZ7Y?si=d3ar53p4vchx1-F2&t=18908)  

Après les bâtiments, les chargeurs de voitures et les serveurs SAP, place à la sécurité des navigateurs, et notamment l'exploitation des permissions qui leur sont octroyées, explicitement par l'utilisateur ou bien via les policies du site visité.  

Il s'avère qu'une mauvaise gestion des permissions dans les IFrames d'un site pouvait être exploitée, notamment via les fenêtres de chat support, permettant des exécutions de code sur le poste de l'ingénieur support, voire une prise de contrôle de son compte.  
Encore une fois, les vulnérabilités présentées ici ont été signalées aux éditeurs, qui les ont corrigées.  

Voici les sketchnotes, dernières que j'ai prises lors de la conférence.  

![Browser permissions, Sketchnote 1 sur 2](img/GreHack%202025_11.png "Browser permissions, Sketchnote 1 sur 2")  
![Browser permissions, Sketchnote 2 sur 2](img/GreHack%202025_12.png "Browser permissions, Sketchnote 2 sur 2")  

## Channel Binding with MSSQL: A Deep Dive into TDS, NTLM and STARTTLS Madness  
[Aurélien Chalot](https://www.linkedin.com/in/aurelienchalotinc/?originalSubdomain=fr)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=oEFPyyfADW4csPvK&t=20829)  

Aurélien nous a présenté comment une demande de feature sur l'outil NetExec s'est transformé en chemin de croix parsemé d'analyse réseau et cryptographie.  
L'article de blog traitant de ce sujet est disponible ici : https://blog.whiteflag.io/blog/a-journey-about-mssql/.  

## From YAML to Root: CI/CD Pipeline Attacks and Countermeasures
[Hugo Ferreira dos Santos](https://www.linkedin.com/in/hugo-ferreira-dos-santos-625099133/)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=tNnRpEk6jnnsQbkG&t=23071)  

Les pipelines d'intégration et livraison continue ne sont pas épargnées par les failles de sécurité.  
Et notamment, lorsque les infrastructures ne sont pas correctement protégées, on peut exécuter du code sur le serveur hébergeant les pipelines, ou encore obtenir un shell, le transformant en point d'attaque vers le reste de l'infrastructure.  

## Sharker: where Wireshark ends, we begin
[Pierre Milioni](https://www.linkedin.com/in/pierremilioni/)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=utiqs7QOQ4aWSBNy&t=27355)  

La cybersécurité, c'est aussi créer des outils, comme ici [Sharker](https://github.com/synacktiv/sharker) créé par Synaktiv, dont l'objectif est d'effectuer un premier filtre sur une capture réseau obtenue via Wireshark.  
Pierre est venu présenter cet outil, et son fonctionnement.  

## So you want to start RadioHacking ?
[Noë Flatreaud](https://nflatrea.bearblog.dev/about/)  

[Captation vidéo](https://www.youtube.com/live/F4CudbWHZ7Y?si=pFZ_PD-6dWyTLuTh&t=28720).

Je n'ai pas pu assister à ce talk à cause du retard pris par la conférence.  

## Conclusion

Cette première venue à GreHack était très intéressante, mais aussi plus intense que les autres conférences auxquelles j'assiste habituellement (preuve en est le nombre réduit de sketchnotes).  
N'étant pas moi-même dans les pentest ou le reverse-engineering, j'ai du fournir un effort supplémentaire pour suivre les talks. De plus, le fait qu'ils soient en anglais ajoute un peu de charge à tout cela.  

J'ai apprécié la diversité des sujets, mais je ne saurai juger de leur qualité/pertinence d'un point de vue technique.  
Le déroulé de la journée a été un peu compliqué je trouve, la conférence a pris pas mal de retard ce qui a été assez frustrant.  
La prochaine fois je pense venir également aux workshops et au CFT (s'il reste de la place dans l'équipe Quarkslab 🙂).
