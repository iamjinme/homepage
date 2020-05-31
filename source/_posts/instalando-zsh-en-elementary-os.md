---
title: Instalando ZSH en ElementaryOS
date: 2019-03-13 17:45:25
tags:
  - elementary os
  - zsh
  - dark theme
---
Honestamente cuando no estoy programando, suelo usar mucho la consola de GNU/Linux para hacer la mayoria de las tareas, así que me gusta que tenga un buen *look*; para ello instalo Z-shell (Oh My Zsh) con un tema compatible con [Git](https://git-scm.com/), en este caso **agnoster**. A continuación te explico como instalarlo:

## Actualiza los repositorios
Lo primero es verificar que tienes los repositorios actualizados, ejecuta lo siguiente en consola:

``` bash
$ sudo apt-get update
$ sudo apt upgrade
```

## Instala ZSH y las fuentes Powerline
Instalamos la aplicación principal y las fuentes que necesitará el tema que configuraremos:

``` bash
$ sudo apt install zsh
$ sudo apt-get install powerline fonts-powerline
```

## Clona el repositorio Oh My Zsh
Necesitamos obtener un archivo de configuración básico, asi que ejecutamos lo siguiente:

``` bash
$ git clone https://github.com/robbyrussell/oh-my-zsh.git ~/.oh-my-zsh
$ cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
```

## Edita el archivo de configuración
Para configurar el tema por defecto editamos `.zshrc` con el editor nano en nuestra carpeta personal y buscamos la linea `ZSH_THEME="robbyrussell"` cambiando *robbyrussell* por **agnoster** y salvamos el archivo con *Ctrl-X* y *Enter*.

``` bash
$ nano .zshrc
$ ZSH_THEME="agnoster"
```

## Configura ZSH por defecto
Sólo nos queda configurar ZSH para que sustituya a `bash`, en consola escribimos:

``` bash
$ chsh -s /bin/zsh
```
Ahora toca reiniciar o salir de la consola para que se vean los cambios reflejados. **Qué te ha parecido el tutorial, sencillo?** Dejanos tus comentarios.