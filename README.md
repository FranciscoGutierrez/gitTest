# Introducción a Git
Hola, esta es una pequeña guía con el objetivo de introducirse a Git.
##¡Manos a la obra!
####Instalar Git:
* **Ubuntu**: $ apt-get install git
* **Otra distribución**: http://git-scm.com/download/linux
* **Windows**: http://git-scm.com/download/win
* **Mac**: $ brew install git

**Brew** es un administrador de paquetes para Mac. (Altamente recomendado).

##Iniciar Git, First Commit
Vamos a trabajar con Git, primero crearemos el repositorio.
```shell
$ git --version #Checar la existencia de Git
$ mkdir GitTest #Creamos una carpeta.
$ cd GitTest    #Nos movemos a la carpeta.
$ git init      #Iniciar aquí mismo un repositorio.
$ git status    #Checamos el estado de Git.
```
A continuación agregamos un archivo:
```shell
$ vim HelloWorld.txt
```
>*Para este caso utilizaré Vim que es un editor en Terminal pero pueden ocupar cualquier editor, solo asegúrense de guardar el archivo en la carpeta. Para los mas aventurados, Vim es un editor potente y muy interesante.*

>Dentro de **Vim** escribimos "Hola mundo" presionamos <kbd>esc</kbd> y a continuación <kbd>:w</kbd> para guardar cambios y despues <kbd>:q</kbd> para salir.

Ahora revisamos el directorio:
```shell
$ ls
```
Vamos a decirle a Git que hemos hecho cambios y queremos que añada el nuevo archivo al repositorio:
```shell
$ git status #El estado del repositorio ha cambiado (new files).
$ git add .  #Le decimos a Git que añada todos los archivos.
$ git status #Nuevos archivos, listos para commit.
$ git commit -a -m "Primer commit, HelloWorld"
```
**FYI**:
* <kbd>-a</kbd> Toma en cuenta todos los archivos cambiados.
* <kbd>-m</kbd> Vamos a enviar un mensaje que describa el commit.

## Push a un repositorio remoto (Github)
1. Copiar la URL del repositorio.
2. En mi caso: https://github.com/FranciscoGutierrez/gitTest.git

```shell
$ git remote add origin <remote repository URL>
# Establece el nuevo repositorio remoto.
git remote -v
# Verifica la URL del repositorio remoto.
```
Una vez que conocemos el repositorio remoto, debemos integrar ambos repositorios:
```shell
$ git pull origin master
# para traer el contenido del repositorio remoto al repositorio local.
$ git push origin master
# para enviar los cambios del repositorio local al remoto.
```
## Commit, Push, Commit, Push
Ahora modifiquemos nuevamente el archivo local:
```shell
$ vim HelloWorld.txt
# Ahora queremos que el archivo diga, "Me gusta mucho Git."
# recuerda esc - :w - :q para guardar cambios y salir en Vim.
$ git status
# Siempre checamos el estado de Git.
# Git me dice que hay cambios.
$ git commit -a -m "Se agregó una nueva línea"
$ git push
# ¡Ya estamos trabajando con Git y GitHub!
```
## Add, Commit, Push
Ahora agreguemos un nuevo archivo:
```shell
$ vim NuevoArchivo.txt
$ git status
# Siempre checamos el estado de Git.
$ git add .
#Le decimos a Git que añada todos los archivos.
$ git status
# Checamos el estado de Git.
$ git commit -a -m "Se agregó un nuevo archivo"
$ git push
```

## Contribuir mediante Fork & Pull
Primero que nada hay que hacer Fork al repositorio:
https://github.com/FranciscoGutierrez/gitTest
<img src="http://cl.ly/image/2k1A2s3Q2R2z/Screen%20Shot%202014-10-23%20at%206.45.01%20PM.png
" alt="alt text" style="width:200px;height:auto">

Fork hace una copia del repositorio a su cuenta de Git, ya dentro de tu cuenta de Git debes seguir los siguientes pasos para realizar un pull request:

```shell
$ git clone https://github.com/<git-my-username>/gitTest.git
$ cd gitTest
# Cambiamos de directorio y agregamos un archivo <my-id>.txt
$ vim <my.id>.txt
# dentro del archivo escriban su nombre.
$ git status
# Checamos el estado de Git.
$ git commit -a -m "Escribí mi nombre"
$ git push
# Hacemos commit y push.
```
> **Importante**: El archivo debe llevar como nombre tu id y adentro de este archivo debe ir escrito tu nombre.

Por último vamos a Github y dentro de tu repositorio "gitTest", en tu cuenta de git, hacemos pull request presionando el siguiente ícono de color **verde**:


<img src="http://cl.ly/image/2f1L0T220k3B/fork.png" alt="alt text" style="width:200px;height:150px">

Seguimos los pasos y enviamos el Pull Request.

## Contacto:
**Facebook**: fsalvador23@gmail.com
