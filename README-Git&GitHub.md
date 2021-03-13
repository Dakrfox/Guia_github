# Guía github. 🚀
_Esta guia esta creada como referencia para los comandos github que yo voy a utilizar mas frecuentemente
esto no quiere decir que a alguien no le sirva, simplemente los escribire Segun vea conveniente._
## Comandos: 
* git add (archivo que se quiere agregar) - (. para agregar todos los archivos) 
* git commit, para identificar los cambios (siempre agregalo despues del git add), para agregar comentario se le pone -m "aqui el comentario y si incluye las comillas"
* git status -s, te hara ver los archivos y si estan agregados o no al repositorio pd. si todo esta agregado no te va a aparecer nada.
* git log --oneline, descripcion de los commit
* git reset --hard codigo del commit ( con el comando de arriba se puede saber el codigo [en gitbash aparece de primero y de color amarillo] al que queremos retornar)

_se pueden usar el comando add cuando se requiera sin embargo si no hay nada que agregar simplemente mostrar que no hay nada que agregar, si se agrego un archivo nuevo se hara
si se edito uno... no habria necesidad nada mas de agregar un commit. Sin embargo podemos usar -am para agregar y al mismo tiempo agregar una descripcion como:_


```
$ git commit -am "escribe comentario aqui y no se te olviden las comillas por favor"

```
# Vim
_Es un editor dentro de git, con el podemos modificar cosas como si no escribiste bien un commit_ 

```
$ git commit --amend 
``` 
_aqui estaremos dentro del editor, borramos en la parte de arriba luego le damos ESC y en la parte de abajo escribimos la nueva descripcion. ENTER Y ESC y seguimos 
con el comando :wq para guarda y salir_ 
