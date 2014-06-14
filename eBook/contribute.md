# Guía para colaborar con el proyecto

Esta va a ser una pequeña guía donde se va a describir como se puede aportar en este proyecto en la traducción, corrección y actualización.

Para esto vamos a explicar como copiar lo que se ha realizado hasta el momento (realizar un fork), guardarlo en tu PC (realizar un clone), y enviarnos tus aportes (realizar un pull request).
Para que de esta forma podamos agregar tu aporte al proyecto sin que se tengan inconvenientes.

***

## Trabajando con github

El esquema de trabajo que nos propone **github** puede parecer confuso al principio, pero en realidad es bastante simple, tan sólo hay que tener presente que uno está trabajando con tres repositorios distintos y entender el rol que cada uno cumple.

**Repositorio upstream:** es el repositorio en github de la aplicación con la cual vamos a colaborar. En nuestro caso el repositorio está en https://github.com/Jackgris/wikiLibGDX_es. No podremos hacer ningún cambio directamente sobre este repositorio, ya que no tendremos permisos de escritura sobre el mismo. Lo que haremos es crear nuestra propia copia (fork) del mismo.

**Repositorio origin:** es nuestra copia del repositorio que forkeamos alojada en github. A este repositorio enviaremos los cambios que efectuaremos en nuestro repositorio local.

**Repositorio local:** es el repositorio local que tendremos en nuestra propia estación de trabajo (o PC).

Comúnmente realizaremos los cambios trabajando en nuestro repositorio local. Cuando hayamos confirmado (realizando un commit) nuestros cambios localmente, los enviaremos (haciendo un push) a nuestro repositorio origin alojado en github. Luego haremos un pedido (o pull request) al repositorio upstream solicitándole que integre los cambios del repositorio origin.

Este es el esquema general de trabajo con github, que nos servirá no sólo para colaborar con esta traducción, sino con cualquier proyecto libre alojado en **github**, incluido el propio framework **Libgdx**.

***

## Crear una cuenta en github

Lo primero que tendremos que hacer es navegar a https://github.com/signup/free y crear una cuenta gratuita en **github**.

Luego deberás instalar git en tu equipo y configurar tu cuenta siguiendo las instrucciones para Linux, Mac OS o para windows, según el sistema operativo que estés utilizando.

***

## Hacer un fork del repositorio upstream

Navega al sitio de **github** e ingresa con tu usuario y password. Luego tendrás que navegar a https://github.com/Jackgris/wikiLibGDX_es y hacer clic en **“fork”**. Con esto ya habrás creado tu repositorio origin.

***

## Clonar nuestro repositorio origin en un repositorio local

En nuestra estación de trabajo ejecutamos las siguientes instrucciones (debes ajustarlas según tu nombre de usuario, remplazando `[tu_cuenta_de_github]` por tu nombre):

    cd ~
    mkdir apps
    cd apps
    git clone git@github.com:[tu_cuenta_de_github]/wikiLibGDX_es.git

De esta manera nos quedará nuestra copia en `~/apps/wikiLibGDX_es`. Para traducir la documentación sigue los pasos que se encuentran abajo en la guía. 

***

## Guardar los cambios y enviar nuestras traducciones

Una vez que hemos terminado de traducir algún archivo, vamos a querer enviarlo al administrador de **wikiLibGDX_es** para que sean incluidos en producción. Para ello tendremos que confirmar los cambios en nuestro repositorio local, actualizar nuestro repositorio origin en **github**, y hacer un pedido para que estos cambios sean incluido en el repostiorio upstream.

Mediante el comando git status podemos ver los archivos que hemos modificado localmente. Con el comando **git add**, le indicamos a git cuáles son los archivos que vamos a querer confirmar (commit). Con **git commit** confirmamos los cambios en nuestro repositorio local y finalmente, con **git push origin master** subimos los cambios locales a nuestro repositorio origin. Situados en el directorio del repositorio, en nuestro ejemplo `~/apps/wikiLibGDX_es`, estos serían los comandos que deberemos ejecutar:

    git status
    git add .
    git commit -m "traduje una nueva página"
    git push origin master

En caso de haber cargado un incidente para esa página, es sumamente útil incluir el texto fixes seguido del signo `#` y el número del incidente (o **issue**) en el texto que utilizamos al hacer el commit, de la siguiente manera `git commit -m "fixes #34 - traduje una nueva página"`. De esta manera **github** relacionará nuestros cambios con el incidente y lo cerrará automáticamente.

Luego navegamos a nuestro repositorio origin, en este caso `https://github.com/[nuestro-usuario]/wikiLibGDX_es`, en donde ya deberías poder ver los cambios que acabamos de subir. Para solicitar al repositorio upstream que integre nuestros cambios simplemente hacemos clic en el botón pull request. Y ahora tan sólo resta esperar que el administrador del repositorio upstream (en este caso **jackgris**) revise los cambios y los impacten en la aplicación.

***

## Manteniendo nuestros repositorios actualizados

A medida que sigamos trabajando, querremos mantener actualizados nuestros repositorios (local y origin) con los cambios del repositorio upstream. Para eso configuramos el repositorio upstream como un repositorio remoto (remote) vinculado a nuestro repositorio local. Situados en el directorio del repositorio, en nuestro ejemplo `~/apps/wikiLibGDX_es`, deberemos ejecutar:

    git remote add upstream git@github.com:Jackgris/wikiLibGDX_es.git

Cuando querramos traer las actualizaciones de upstream, deberemos ejecutar:

    git fetch upstream
    git merge upstream/master

***

## Crear un nuevo archivo



## Sintaxis 




## Enlaces

- [Inicio](../README.md)
- [Indice](preface.md)