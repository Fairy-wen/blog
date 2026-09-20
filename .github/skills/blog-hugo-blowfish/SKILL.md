---
name: blog-hugo-blowfish
description: "Assistant de développement pour un blog Hugo écrit en Markdown et rendu avec le thème Blowfish. À utiliser pour rédiger, relire, corriger, structurer ou publier des articles en français, gérer les images et shortcodes, vérifier les liens et métadonnées, prévisualiser le site ou lancer un build Hugo."
argument-hint: "Décrivez l'article, la correction ou la vérification à effectuer dans le blog."
user-invocable: true
disable-model-invocation: false
---

# Blog Hugo avec Blowfish

## Mission

Maintenir le blog dans `blog/` en respectant Hugo, Markdown, le thème Blowfish et le ton éditorial existant. Produire des changements directement utilisables et laisser les fichiers générés hors du périmètre des modifications manuelles.

## Quand utiliser cette compétence

- Créer ou enrichir un article sous `content/`.
- Relire la langue, la structure, les liens ou les métadonnées d'un article.
- Ajouter ou référencer des images dans un page bundle.
- Utiliser ou diagnostiquer un shortcode Hugo ou Blowfish.
- Vérifier le rendu local, les liens et le build du site.
- Modifier une mise en page ou un composant du blog lorsque le contenu seul ne suffit pas.

## Procédure

1. Identifier la page, le layout, le shortcode ou la configuration qui possède réellement le comportement demandé. Lire le fichier ciblé et un exemple voisin avant de modifier quoi que ce soit.
2. Déterminer le type de contenu et conserver sa structure locale. Pour un nouvel article, préférer un page bundle sous `content/articles/` avec un `index.md` et ses médias voisins.
3. Préserver le frontmatter existant. Pour les articles du blog, utiliser le format TOML entre `+++` et vérifier au minimum `title`, `date`, `tags` et `categories` quand ils sont pertinents.
4. Rédiger en français avec une voix personnelle et lisible. Corriger les fautes et les formulations ambiguës sans réécrire inutilement le style de l'autrice. Conserver les accents et les liens utiles.
5. Référencer les médias avec des chemins relatifs au page bundle. Vérifier que chaque fichier existe, que le texte alternatif est descriptif et que les images ne sont pas copiées dans `public/`, qui est une sortie générée.
6. Réutiliser les shortcodes déjà présents dans le dépôt, notamment `carousel`, `gallery` et ceux fournis par Blowfish. Vérifier leur syntaxe dans un exemple local ou dans le thème avant d'en introduire un nouveau.
7. Pour une modification de présentation, inspecter d'abord `layouts/`, `assets/`, `static/` et la configuration Hugo. Préférer le mécanisme Hugo ou Blowfish existant à une duplication CSS ou HTML.
8. Vérifier les liens relatifs, les ancres, les taxonomies et les références d'images. Ne pas inventer de destination ; signaler les URL externes incertaines plutôt que de les remplacer silencieusement.
9. Construire le site depuis la racine du dépôt avec `hugo --gc --minify`. Pour examiner le rendu interactif, utiliser `hugo server -D` puis vérifier la page concernée dans le navigateur.
10. Résumer les fichiers modifiés, les vérifications exécutées et les éventuels points restant à confirmer.

## Règles de travail

- Ne pas modifier `public/` ni `resources/_gen/` manuellement.
- Ne pas supprimer les changements existants qui ne sont pas liés à la demande.
- Garder les changements ciblés et préserver le style des fichiers voisins.
- Éviter les shortcodes ou paramètres Blowfish non vérifiés.
- Ne pas ajouter de dépendance ou de script quand Hugo et les outils déjà présents suffisent.
- Pour une correction éditoriale, distinguer clairement une faute certaine d'une préférence stylistique.
- Si le build échoue pour une raison indépendante de la modification, donner l'erreur exacte et poursuivre les contrôles locaux possibles.

## Contrôle de fin

Avant de conclure, vérifier :

- le frontmatter est valide et cohérent avec la page ;
- les fichiers locaux référencés existent ;
- les liens et shortcodes ajoutés sont plausibles ;
- `hugo --gc --minify` réussit, ou son erreur est documentée ;
- aucun fichier généré n'a été édité pour obtenir le résultat ;
- le résumé final mentionne les validations réellement effectuées.
