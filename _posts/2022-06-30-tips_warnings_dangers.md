---
title: Conseils, Avertissements et Dangers
author: Tao He
date: 2022-06-30
category: Jekyll
layout: post
---

Le thème jekyll-theme supporte les blocs conseil, avertissement et danger, dont le style provient du [site discord.js][1].

Vous pouvez utiliser les [attributs markdown (supportés par kramdown)][2] suivants :

### Conseils

En utilisant un attribut `{: .block-tip}` :

```markdown
> ##### CONSEIL
>
> Ce guide a été testé avec @napi-rs/canvas^0.1.20, assurez-vous donc d'avoir
> cette version (ou similaire) après l'installation.
{: .block-tip }
```

> ##### CONSEIL
>
> Ce guide a été testé avec @napi-rs/canvas^0.1.20, assurez-vous donc d'avoir
> cette version (ou similaire) après l'installation.
{: .block-tip }

### Avertissements

En utilisant un attribut `{: .block-warning}` :

```markdown
> ##### AVERTISSEMENT
>
> Assurez-vous d'être familier des concepts tels que async/await et la déstructuration d'objets
> avant de continuer, car nous allons utiliser des fonctions de ce genre.
{: .block-warning }
```

> ##### AVERTISSEMENT
>
> Assurez-vous d'être familier des concepts tels que async/await et la déstructuration d'objets
> avant de continuer, car nous allons utiliser des fonctions de ce genre.
{: .block-warning }

### Dangers

En utilisant un attribut `{: .block-danger}` :

```markdown
> ##### DANGER
>
> Vous ne pouvez pas supprimer un message éphémère.
{: .block-danger }
```

> ##### DANGER
>
> Vous ne pouvez pas supprimer un message éphémère.
{: .block-danger }

[1]: https://discordjs.guide/popular-topics/canvas.html#setting-up-napi-rs-canvas
[2]: https://kramdown.gettalong.org/quickref.html#block-attributes
