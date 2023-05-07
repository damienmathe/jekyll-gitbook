---
title: Tableaux larges
author: Tao He
date: 2022-06-26
category: Jekyll
layout: post
---

Un tableau large doit être imbriqué dans une balise `div` avec la classe `table-wrapper`
afin d'assurer son affichage correct sur les appareils mobiles. Par exemple :

```markdown
<div class="table-wrapper" markdown="block">

|titre1|titre2|titre3|titre4|titre5|titre6|titre7|titre8|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|1|2|3|4|5|6|7|8|
|1|2|3|4|5|6|7|8|
|1|2|3|4|5|6|7|8|
|1|2|3|4|5|6|7|8|

</div>
```

Sera rendu de cette façon :

<div class="table-wrapper" markdown="block">

|titre1|titre2|titre3|titre4|titre5|titre6|titre7|titre8|
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
|1|2|3|4|5|6|7|8|
|1|2|3|4|5|6|7|8|
|1|2|3|4|5|6|7|8|
|1|2|3|4|5|6|7|8|

</div>
