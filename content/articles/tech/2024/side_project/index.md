+++
title = "Mon premier side-project"
suumary = "Pourquoi je l'ai créé, qu'est-ce que j'en retire ?"
date = 2024-10-01
tags = ["billet", "développement"]
categories = ["tech"]
+++


# Il était une fois

En juin 2024, alors que j'étais en recherche d'emploi, j'ai initié un projet perso en utilisant des techno et langages que je ne connaissais pas, aidée de ChatGPT et divers guides de développement sur le net.  

Pourquoi vouloir faire ça ? Quel en est le bilan en cet automne 2024 ?

# Le jour où tout bascule

Parmi les entreprises que je sollicite lors de mes recherches, il y en a une qui évolue dans le monde du cloud, et du déploiement automatisé des solutions de ses clients.  
Mon CV arrive dans les mains du responsable du secteur support entre autres, qui malheureusement ne retient pas ma candidature notamment parce qu'à cet instant ils n'ont pas de poste ouvert.  

Dans sa réponse, le responsable me précise aussi qu'il manque à mon parcours les technos utilisées principalement par leurs clients, et que cela manque pour adresser ce rôle dans leur entreprise.  
J'ai beaucoup apprécié sa réponse car elle était très détaillée, construite, et ne constituait pas un simple refus que j'aurais pu vivre comme un échec de plus, mais comme une opportunité de m'améliorer.  

# On se relève les manches

Suite à cette réponse, je remets en question l'adéquation de mes compétences vis-à-vis des postes et entreprises ciblées.  
On ne va pas chercher midi à quatorze heure, je décide alors de (me) prouver que je peux ajouter des cordes à mon arc.  

Je choisis ainsi de mettre le nez dans les technos qui ont le vent en poupe selon mes critères de recherche d'emploi, telles que suggérées par mon ChatGPT : `Node.js`, `PostgreSQL` et `Docker`.  

Le meilleur moyen me semble l'apprentissage par la pratique, avec un side-project dédié, hébergé sur `GitHub`, et public. Comme ça, c'est facile à montrer en processus de recrutement.  

Après quelques échanges de prompt, j'arrête mon choix sur une application de partage de recettes de cuisine. Si le projet est convaincant, je pourrai l'utiliser à titre personnel (c'est toujours mieux d'être le·la premier·ère utilisateurice de son produit 😜).  

# Deep dive

L'ennui quand on veut commencer un projet avec plein de technos que l'on ne maîtrise pas dedans, c'est que ça prend pas mal de temps pour avoir la "coquille vide", à savoir dans mon cas une image `Docker` qui expose une page web dont les données sont stockées sur une base `PostgreSQL`. J'aurais pu commencer par lire l'ouvrage ["Understanding Docker in a visual way"](https://www.amazon.com/Understanding-Docker-visual-way-sketchnotes/dp/B0BT6ZXR1W) écrit et dessiné par [Aurélie Vache](https://x.com/aurelievache) me direz-vous, ou même regarder ses vidéos, mais c'est plus drôle de sauter à pieds joints dans le vif du sujet.

![Un renard qui saute la tête la première dans la neige](./img/cute-fox-5-times.gif "Un renard qui saute la tête la première dans la neige")


J'ai vais petit à petit, en créant d'abord le conteneur, puis la base de données, et les première briques `CRUD` (Create, Read, Update, Delete).
Je fais ça en utilisant à la fois ChatGPT pour m'aider à comprendre ce qui peut ne pas marcher, mais également grâce à quelques ressources sur le net qui me permettent d'aborder les différentes couches techniques.  

En l'occurrence : 
- pour la partie `Node.js` :  
  + https://www.tutorialspoint.com/nodejs/nodejs_express_framework.htm  
  + https://developer.mozilla.org/en-US/docs/Learn/Server-side/Express_Nodejs  
- pour tester un rendu `html` + `css` : https://codepen.io/  
- pour l'accès base de données : https://sequelize.org/docs/v6/ _(Quelle joie de découvrir le monde des ORM (Object-Relational Mapping) !_

Autant de concepts à associer ensemble, puisque je comprends alors toutes les blagues sur la quantité de frameworks `Javascript` qui existent, ainsi que les multiples API disponibles. Et bien évidemment les tutos dont je m'inspire n'utilisent pas forcément les mêmes API que moi. Il faut alors extraire le concept et le transposer pour arriver à ses fins. 

Je me heurte forcément à pas mal de problèmes pour intégrer les différentes couches techniques, et c'est là que l'esprit baby-steps est important.  
On résout un problème à la fois, et on n'essaye pas de tout faire d'un coup. Je n'arrive pas à intégrer `Boostrap` dans mon projet ? Pas grave, l'interface fonctionne, on la rendra conviviale plus tard.  
Au-delà de l'apprentissage technologique, c'est pour moi un bon moyen de me forcer à prioriser et avoir des attentes raisonnables.  

# Le bilan

A l'heure où j'écris ces lignes (octobre 2024), mon code me permet d'ajouter des recettes, de les lister et de les consulter.  
Je ne peux ni les modifier, ni les supprimer, le site est en `http` non sécurisé et ne gère pas l'authentification.  

Mais c'est OK, le but n'est pas de le mettre en prod dans l'immédiat, le but est d'apprendre.  
Je pense d'ailleurs qu'avant de reprendre le développements des fonctionnalités, je vais m'attarder un peu sur la théorie autour de `Docker` d'une part, et surtout sur le concept des `routeurs` et `controllers`, car je dois avouer que pour le moment j'applique ce que je vois dans les tutos, mais j'aurais du mal à expliquer de mémoire pourquoi et comment on les utilise.  

L'avantage de (re)voir l'aspect théorique après avoir pratiqué, pour moi, c'est que cela me permet de raccrocher les wagons entre ce que je lis et ce que j'ai produit, cela m'aide à comprendre beaucoup plus efficacement.  

Je compte continuer à développer ce side-project à mon rythme, pour le plaisir d'apprendre et de créer quelque chose, parmi mes multiples autres occupations !

Pour les curieux·ses, le repo est par ici :  

{{< github repo="Fairy-wen/app-recettes" >}}  


# Bonus

J'ai demandé sur les réseaux ce qui avait motivé les gens à créer un side-project. A ma grande surprise, les raisons principales sont pour apprendre quelque chose, ou sans raison particulière (j'imagine "pour le fun").  
Naïvement j'imaginais que le motif principal aurait été pour répondre à un besoin métier perso, mais il semblerait que non, comme quoi...  

<blockquote class="twitter-tweet" data-theme="dark"><p lang="fr" dir="ltr">Bonjour la communauté dev !<br><br>Parmi celles et ceux qui ont monté un ou plusieurs side-project, quelle en a été la principale raison ?<br><br>C&#39;est pour un billet de blog, merci !<br>RT appréciés.</p>&mdash; Virginie Pageaud (Casavecchia) - looking for a job (@La_Fee_Dragee) <a href="https://twitter.com/La_Fee_Dragee/status/1840652261413806414?ref_src=twsrc%5Etfw">September 30, 2024</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>