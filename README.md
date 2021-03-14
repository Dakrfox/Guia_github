# Guía github. 🚀
_Esta guia esta creada como referencia para los comandos github que yo voy a utilizar mas frecuentemente
esto no quiere decir que a alguien no le sirva, simplemente los escribire Segun vea conveniente._
## usuario y correo en git
```
$ git config --global user.name "tu nombre aqui"
$ git config --global user.email tu correo aquí
```
## Comandos: 
* `git add (archivo que se quiere agregar) - (. para agregar todos los archivos) `
* `git commit`, para identificar los cambios (siempre agregalo despues del git add), para agregar comentario se le pone -m "aqui el comentario y si incluye las comillas"
* `git status -s`, te hara ver los archivos y si estan agregados o no al repositorio pd. si todo esta agregado no te va a aparecer nada.
* `git log --oneline`, descripcion de los commit
* `git reset --hard codigo del commit` ( con el comando de arriba se puede saber el codigo (en gitbash aparece de primero y de color amarillo) al que queremos retornar)

_se pueden usar el comando add cuando se requiera sin embargo si no hay nada que agregar simplemente mostrar que no hay nada que agregar, si se agrego un archivo nuevo se hara
si se edito uno... no habria necesidad nada mas de agregar un commit. Sin embargo podemos usar -am para agregar y al mismo tiempo agregar una descripcion como:_


```
$ git commit -am "escribe comentario aqui y no se te olviden las comillas por favor"

```
## Vim
_Es un editor dentro de git, con el podemos modificar cosas como si no escribiste bien un `commit`_ 

```
$ git commit --amend 
``` 
_aqui estaremos dentro del editor, borramos en la parte de arriba luego le damos ESC y en la parte de abajo escribimos la nueva descripcion. ENTER Y ESC y seguimos 
con el comando :wq para guarda y salir_ 

# GitHub
_Subir de git a github (del repositorio local a la nube._


* `git init`: inicializas el git en tu repositorio
* `git add README.md`: documento para previsualizar la decripcion del repositorio
* `git commit -m "first commit"`: ya hablamos de esto
* `git branch -M main`: es para crear la rama de nombre main y decirle que va a ser la propia, la master pero teniendo en cuenta la semantica 
* `git remote add origin https://github.com/"tu usuario aqui, sin las comillas"/"nombre".git`: agregar un repositorio local al repositorio de GitHub, teniendo en cuenta que ya debe de estar creado
* `git push -u origin main`: enviarlo para que se publique y que lo puedas visualizar en el repositorio que encuentras en la web.

_nota: la primera vez pide usuario y contraseña de GitHub, no confundir con el de Git_

#### SUGERENCIA: cuando estes haciendo un proyecto y agregas algo, agregalo en commit luego cuando ya sepas que toda va bien pushealo, el push hazlo si vas a dejar hasta ahi el proyecto en el dia, solo para que lo tengas en la nube y no se te pierda

#### RECUERDA: cuando tengas varios commits se especifico porque ahi podras encontrar el codigo tal y como lo guardaste en el y puedes acceder si encuentras un boton con los simbolos **< >** digamos que es un versionamiento

## Para enviar un proyecto al repositorio

* `$git remote add` origin https://github.com/"usuario sin comillas"/"nombre del archivo sin comillas".git esto va a dirigir los archivos que tengas a la ruta del repositorio 
* `$git branch -M main` Aquí por el tema de #BLM te sugieren cambiar la semantica de master a main, (pasa igual con las palabras clave slave, blacklist, whitelist) -M lo vuelve princpal 
* `$git push -u origin main`
```
origin
```
`origin` es una abreviacion  para el repositorio remoto, es una forma de decirle a github de donde viene el proyecto y que asi sea mas facil obtenerlo ( esto se usa en vez de una url del link local )

## TAGS
_tags es una manera de representar una rama inalterable, tiene una version del proyecto la cual no se puede modificar como se hace en un rama_
crear tag 

`$git tag "nombre"` (version se abrevia coo v eejemp´lo : v1) `-m` "descripcion"

luego para que aparezca en el remoto
```
$git push --tags 
```
## Branchs
_las ramas es la manera de estar trabajando en el mismo proyecto sin dañar el pricipal. Si quieres intentar agregar un cambio un evento o x cosa puedes crear una rama y esta aunque le des push no afectara a la principal_

* `git branch "nombre de la rama sin comillas"` creacion de la rama
* `git branch` te muestra que ramas hay y en cual estamos trabajando
* `git checkout "nombre de la rama sin comillas"`


#### RECUERDA: hay que usar `add`,` commit` y` push` en la rama 

### Merge
_para unir dos ramas, necesitamos situarnos con ` checkout` en la rama destino por ejemplo si se hara un merge desde rama1 a master/main nos situamo en la rama master/main y desde ahi_
```
$git merge "nombre de la rama sin comillas"
```
puede haber conflicto si se toca la misma linea o se modifica ambos el mismo lugar
_estoy abierto a correciones y comentarios_





