+++
title = "Comment prévoir ses articles à l'avance"
date = 2024-06-07
draft = true
tags = ["tuto","blogging"]
categories = ["tech"]
# series = ["Automatiser la publication de contenu sur les réseaux"]
# series_order = 1
+++

# Pourquoi ce besoin ?

Vous le savez peut-être, mais j'essaye tant que possible de partager chaque vendredi de la musique à découvrir.  
Comme toute bonne créatrice de contenu, il est m'est vite apparu indispensable de préparer à l'avance ces publications grâce à [buffer](https://buffer.com/).  

Avec la [refonte du blog]({{< ref "/articles/tech/2024/migration_blog" >}}), j'ai voulu avoir la possibilité de préparer également des articles à l'avance, qui seraient publiés le moment voulu sans action de ma part.  

# Mise en place

La mise en place de la publication automatique est très simple à faire, en combinant les fonctionnalités d'[Hugo](https://gohugo.io/) et des [GitHub Actions](https://docs.github.com/fr/actions).  

## Côté code source du blog

Un article qui sera construit par `Hugo` consiste grossièrement en un fichier rédigé au format `Markdown`.  
Et en en-tête de ce fichier, on place ce que l'on appelle le `front matter`, un bloc de code au format `yaml` permettant de définir quelques propriétés.  

Voici par exemple celui de cet article : 
```markdown
+++
title = "Comment prévoir ses articles à l'avance"
date = 2024-06-07
draft = false
tags = ["tuto","blogging"]
categories = ["tech"]
+++
```

On remarque la présence du champ `date`, qui permet non seulement d'indiquer la date de rédaction de l'article (que l'on verra sur la page rendue), mais qui sera également consommée par Hugo lors de la construction du site.  
En effet par défaut, il ne génère pas les pages datées [dans le futur](https://gohugo.io/getting-started/configuration/#buildfuture).  

Voilà qui est parfait, il n'y a qu'à indiquer la date de publication souhaitée dans ce paramètre, et mettre en place une génération périodique du site !  

## Côté GitHub