---
title: Moderno enfoque para carga asíncrona de CSS
date: 2019-03-22 14:40:38
tags:
  - css
  - html
  - preload
---
Se han percatado de que cada vez los archivos CSS son más grandes que antes? Con el desarrollo de modernos sitios y el enriquecimiento del estandar CSS3 solemos ver archivos de gran tamaño que embellecen un sitio web pero pueden afectar la carga del mismo. Una solución es la **carga asíncrona**.

## Un enfoque moderno
Afortunadamente, ahora hay un estándar web diseñado específicamente para cargar recursos como CSS de ésta forma: `rel="preload"`. Finalmente, podemos cargar CSS asíncrono sin soluciones de JavaScript. Es una broma? no, no lo es, este método solo requiere un controlador de eventos **onload** para que funcione como lo necesitamos. Aún así, es nuestra mejor opción.

``` bash
<link rel="preload" href="mystyles.css" as="style" onload="this.rel='stylesheet'">
```

Que te parece ésta moderna técnica? Utilizas alguna otra?