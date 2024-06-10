+++
title = "Comment prévoir ses articles à l'avance"
date = 2024-06-10
draft = false
tags = ["tuto","blogging"]
categories = ["tech"]
+++

# Pourquoi ce besoin ?

Vous le savez peut-être, j'essaye tant que possible de partager chaque vendredi sur les réseaux de la musique à découvrir.  
Comme toute bonne créatrice de contenu, il est m'est vite apparu indispensable de préparer à l'avance ces publications grâce à [buffer](https://buffer.com/).  

Avec la [refonte du blog]({{< ref "/articles/tech/2024/migration_blog" >}}), j'ai voulu avoir la possibilité de préparer également des articles à l'avance, qui seraient publiés le moment voulu sans action de ma part.  

# Mise en place

La mise en place de la publication automatique est très simple à faire, en combinant les fonctionnalités d'[Hugo](https://gohugo.io/) et des [GitHub Actions](https://docs.github.com/fr/actions).  

## Côté code source du blog

Un article qui sera construit par `Hugo` consiste grossièrement en un fichier rédigé au format `Markdown`.  
Et en en-tête de ce fichier, on place ce que l'on appelle le `front matter`, un bloc de code au format `yaml` ou `toml` permettant de définir quelques propriétés.  

Voici par exemple celui de cet article : 
```toml
+++
title = "Comment prévoir ses articles à l'avance"
date = 2024-06-10
draft = false
tags = ["tuto","blogging"]
categories = ["tech"]
+++
```

On remarque la présence du champ `date`, qui permet non seulement d'indiquer la date de rédaction de l'article (que l'on verra sur la page rendue), mais qui sera également consommée par Hugo lors de la construction du site.  
En effet par défaut, il ne génère pas les pages datées [dans le futur](https://gohugo.io/getting-started/configuration/#buildfuture).  

Voilà qui est parfait, il n'y a qu'à indiquer la date de publication souhaitée dans ce paramètre, et mettre en place une génération périodique du site !  

## Côté GitHub

Le déploiement du site par `GitHub Actions` est géré par le fichier `.github\workflows\hugo.yml`, créé par GitHub lorsque l'on configure pour la première fois le workflow (il ressemble pas mal à un `Jenkinsfile` pour celleux qui connaissent).  
Dans mon cas, j'avais choisi un déclenchement à chaque `push` sur la branche principale :  
```yml
# Sample workflow for building and deploying a Hugo site to GitHub Pages
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]

# Actions de déploiement
```

J'ai donc ajouté un déclenchement programmé (voir la doc [ici](https://docs.github.com/en/actions/using-workflows/events-that-trigger-workflows#schedule)) tous les vendredis matin (jour de publication des vendredi musique).  
Attention, l'heure est en UTC et il n'est pas possible de spécifier nativement la timezone à l'heure où j'écris ces lignes (une discussion est en cours [ici](https://github.com/orgs/community/discussions/13454)).  

J'ajoute donc le déclenchement programmé dans le fichier `hugo.yml` :  

```yml
# Sample workflow for building and deploying a Hugo site to GitHub Pages
name: Deploy Hugo site to Pages

on:
  # Runs on pushes targeting the default branch
  push:
    branches: ["main"]
  
  # Runs every friday at 5 o'clock AM UTC to publish "vendredi musique" posts
  schedule:
    - cron: '00 05 * * 5'
```

Et c'est tout ! Désormais, en plus de la génération lors de la mise à jour de la branche principale, le site est généré tous les vendredis pour prendre en compte les articles futurs (et ça c'est chouette) !