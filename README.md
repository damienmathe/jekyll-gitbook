---
layout: home
title: Thème GitBook pour Jekyll
permalink: /
---

Pour donner un look GitBook aux sites Jekyll !

## Démo

Démonstration en ligne sur Github Pages: [https://sighingnow.github.io/jekyll-gitbook](https://sighingnow.github.io/jekyll-gitbook)

[![Thèmes Jekyll](https://img.shields.io/badge/featured%20on-JekyllThemes-red.svg)](https://jekyll-themes.com/jekyll-gitbook/)

## Pourquoi Jekyll avec GitBook ?

**GitBook** est un style frontend incroyable pour présenter et organiser des contenus (tels que des chapitres de livre
et blogs) sur le Web. Le processus typique pour déployer **GitBook** sur les [pages GitHub][1] est de compiler des fichiers HTML localement, puis de les pousser vers le référentiel Github, généralement vers la branche `gh-pages`. Toutefois, il est plutôt ennuyeux de répéter une telle charge de travail, et cela complique le contrôle de version via `git` lorsqu'il y a des fichiers HTML générés à intégrer et à supprimer.

Ce thème reprend les styles du site **GitBook** et fournit un modèle pour Jekyll de rendu des documents Markdown en HTML, ainsi l'ensemble du site peut être déployé sur les [pages Github][1] sans générer et télécharger le bundle HTML à chaque fois qu'il y a des modifications apportées au référentiel d'origine.

## Pour bien démarrer

Le thème jekyll-gitbook peut être utilisé comme les autres [thèmes Jekyll][2], et supporte la fonction thème distant (remote theme) sur les [pages Github][1].

Vous pouvez ajouter ce thème Jekyll à votre propre site, soit:

- En créant une [instance][3] (fork) de ce référentiel et en y ajoutant vos articles rédigés en Markdown dans le dossier `_posts`, puis en la poussant (push) vers votre propre référentiel GitHub.
- En l'utilisant en tant que thème distant (remote theme) dans `_config.yml` (comme nous le faisons pour le présent site),

```yaml
remote_theme: sighingnow/jekyll-gitbook
```

### Déploiment local avec `jekyll serve`

Ce thème peut être exécuté localement à l'aide de Ruby et des Gemfiles.

[Tester vos pages GitHub localement avec Jekyll](https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/testing-your-github-pages-site-locally-with-jekyll) - GitHub

## Recherche de texte complet

La fonction de recherche dans le thème jekyll-gitbook est fournie par le module [gitbook-plugin-search-pro][5] et est activée par défaut.

[https://sighingnow.github.io/jekyll-gitbook/?q=generated](https://sighingnow.github.io/jekyll-gitbook/?q=generated)

## Coloration syntaxique

La coloration syntaxique est configurable à l'aide de l'entrée suivante dans le fichier `_config.yaml` :

```yaml
syntax_highlighter_style: colorful
```

Le style de coloration syntaxique par défaut est `colorful`, les styles supportés peuvent être trouvés dans [le référentiel rouge][6]. Des styles personnalisés peuvent être ajoutés dans [./assets/gitbook/rouge/](./assets/gitbook/rouge/).

## Générer une table des matières (TOC)

Le thème jekyll-gitbook fait appel à [jekyll-toc][4] pour générer le *contenu* de la page.
La fonction TOC (table des matières) n'est pas activée par défaut. Pour l'utiliser, modifiez la configuration TOC
dans `_config.yml` :

```yaml
toc:
    enabled: true
    h_min: 1
    h_max: 3
```

## Google Analytics, etc.

Le thème jekyll-gitbook supporte l'implémentation des outils d'analyse de traffic [Google Analytics][7], [CNZZ][8] et [Application Insights][9] grâce à la configuration minimale suivante dans `_config.yaml` :

```yaml
tracker:
  google_analytics: "<VOTRE CLÉ GOOGLE ANALYTICS, p.e, UA-xxxxxx-x>"
```

De la même façon, CNZZ peut être ajouté avec la configuration suivante dans `_config.yaml` :

```yaml
tracker:
  cnzz: "<VOTRE CLÉ CNZZ ANALYTICS, p.e., xxxxxxxx>"
```

Application Insights peut être ajouté avec la configuration suivante dans `_config.yaml` :

```yaml
tracker:
  application_insights: "<VOTRE PHRASE DE CONNEXION POUR APPLICATION INSIGHTS>"
```

## Commentaires Disqus

Les commentaires [Disqus](https://disqus.com/) peuvent être activés en ajoutant la configuration suivante dans `_config.yaml`&nbsp;:

```yaml
disqushandler: "<VOTRE PSEUDONYME DISQUS>"
```

## Feuille de style supplémentaire ou éléments Javascript

Vous pouvez ajouter des styles CSS ou des références JavaScript en utilisant des collections de configuration :

- extra_css: pour les feuilles de style supplémentaires. Si l'URL ne commence pas par `http` ou `https`, le chemin doit être relatif à la racine du site (sans le caractère `/` au début).
- extra_header_js: pour les scripts supplémentaires à ajouter dans la balise `<head>`, après que `extra_css` ait été ajouté. Si l'URL ne commence pas par `http` ou `https`, le chemin doit être relatif à la racine du site (sans le caractère `/` au début).
- extra_footer_js: pour les scripts supplémentaires à ajouter à la fin du document HTML, avant les scripts de tracking. Si l'URL ne commence pas par `http` ou `https`, le chemin doit être relatif à la racine du site (sans le caractère `/` au début).

## Personnalisation des réglages de polices

Les polices de caractères peuvent être personnalisées en modifiant les entrées `.book.font-family-0` et `.book.font-family-1` dans [`./assets/gitbook/custom.css`][10],

```css
.book.font-family-0 {
    font-family: Georgia, serif;
}
.book.font-family-1 {
    font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
}
```

## Blocs Conseil, Avertissement et Danger

Le thème jekyll-gitbook supporte les attributs personnalisés de kramdown (`{: .block-tip }`, `{: .block-warning }`,
`{: .block-danger }`) comme ceux affichés dans [le site web discord.js][11].

Exemple de code :

```markdown
> ##### CONSEIL
>
> Ce guide a été testé avec @napi-rs/canvas^0.1.20, assurez-vous donc d'avoir
> cette version (ou similaire) après l'installation.
{: .block-tip }
```

Le rendu peut être prévisualisé sur cette page :

[https://sighingnow.github.io/jekyll-gitbook/jekyll/2022-06-30-tips_warnings_dangers.html](https://sighingnow.github.io/jekyll-gitbook/jekyll/2022-06-30-tips_warnings_dangers.html)

## Images de couverture dans les pages

Le thème jekyll-gitbook supporte l'ajout d'une image de couverture à une page spécifique en ajoutant un champs `cover` dans les métadonnées de la page :

```diff
  ---
  title: Page avec image de couverture
  author: Tao He
  date: 2022-05-24
  category: Jekyll
  layout: post
+ cover: /assets/jekyll-gitbook/dinosaur.gif
  ---
```

Cet effet peut être prévisualisé sur cette page :

[https://sighingnow.github.io/jekyll-gitbook/jekyll/2022-05-24-page_cover.html](https://sighingnow.github.io/jekyll-gitbook/jekyll/2022-05-24-page_cover.html)

## Licence

Ce projet est en open source sous la licence Apache, version 2.0.

&copy; 2019 Tao He.

[1]: https://pages.github.com
[2]: https://pages.github.com/themes
[3]: https://github.com/sighingnow/jekyll-gitbook/fork
[4]: https://github.com/allejo/jekyll-toc
[5]: https://github.com/gitbook-plugins/gitbook-plugin-search-pro
[6]: https://github.com/rouge-ruby/rouge/tree/master/lib/rouge/themes
[7]: https://analytics.google.com/analytics/web/
[8]: https://www.cnzz.com/
[9]: https://docs.microsoft.com/en-us/azure/azure-monitor/app/app-insights-overview
[10]: https://github.com/sighingnow/jekyll-gitbook/blob/master/gitbook/custom.css
[11]: https://discordjs.guide/popular-topics/canvas.html#setting-up-napi-rs-canvas
[12]: https://rubygems.org/gems/jekyll-remote-theme
[13]: https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/adding-a-theme-to-your-github-pages-site-using-jekyll
[14]: https://github.com/sighingnow/jekyll-gitbook/blob/master/_config.yml
