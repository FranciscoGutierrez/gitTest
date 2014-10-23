# Introducción a Git
Hola, esta es una pequeña guía con el objetivo de introducirse a Git.
##¡Manos a la obra!
####Instalar Git:
* **Ubuntu**: $ apt-get install git
* **Otra distribución**: http://git-scm.com/download/linux
* **Windows**: http://git-scm.com/download/win
* **Mac**: $ brew install git

**Brew** es un administrador de paquetes para Mac. (Altamente recomendado).

##Iniciar Git, first commit.
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
#Para este caso utilizaré Vim que es un editor en Terminal, pero pueden ocupar cualquier editor, solo asegúrense de guardar el archivo en la carpeta. Para los mas aventurados, Vim es un editor potente y muy interesante.
```
Dentro de **Vim** escribimos "Hola mundo" presionamos <kbd>esc</kbd> y a continuación <kbd>:w</kbd> para guardar cambios y despues <kbd>:q</kbd> para salir.

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

## Push a un repositorio remoto (Github).
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
## Commit, Push, Commit, Push.
Ahora modifiquemos nuevamente el archivo local:

```shell
$ vim HelloWorld.txt
# Ahora queremos que el archivo diga, "Me gusta mucho Git."
# recuerda esc - :w - :q para guardar cambios y salir en Vim.
$ git status
# Siempre checamos el estado de Git.
```
