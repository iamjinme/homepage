---
title: Customizar página de inicio en Hexo
date: 2019-03-08 18:19:52
tags: 
  - index
  - hexo
  - blog
---
[Hexo](https://hexo.io/) es un framework rapido, simple y poderoso realizado en Node.js para crear un blog. Si has llegado hasta acá es porque probablemente lo tengas instalado y funcionando, sino prometo postear como instalarlo en tres pasos.

## Cómo cambio la página principal?
Lo primero que intenté hacer fue darle el toque personal al sitio, pero no encontraba la p%&# página inicial. Hexo trabaja con archivos **Markdown**, que son convertidos y desplegados para mostrar el blog.

La solución parte por crear un archivo index.md en el directorio `sources` de tu proyecto. Y luego desinstalar la dependencia que crea la página principal **auto-mágicamente**. Ejecuta éste comando en la consola, sino tu pagina index.md será ignorada:

``` bash
$ npm remove --save hexo-generator-index
```

La proxima vez que generes tu blog, se mostrará la nueva página inicial.

