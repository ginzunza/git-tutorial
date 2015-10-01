# git_tutorial
Comandos fundamentales para comenzar a trabajar con Git
#Lo básico
Una vez que hemos hecho cambios, ya sea, modificar, agregar o eliminar archivos, para incluirlos debemos escribir el siguiente comando:
```git
git add --all
```
Luego, debemos hacer un comentario que explique, en términos globales, lo que se modificó. Para ello debemos escribir el siguiente comando:
```
git commit -m "acá tu comentario"
```
Finalmente, para subir los cambios a una rama de manera remota, debemos escribir el siguiente código:
```
git push origin nombre-rama
```
En el caso de que nuestra rama fuera "master", el código anterior quedaría de la siguiente manera:
```
git push origin master
```
Si quieremos saber en cuál rama nos encontramos, para saber donde subir nuestros cambios, debemos escribir el siguiente comando:
```
git branch
```
Una vez escrito el comando anterior, visualizaremos algo parecido a lo siguiente:
```
  otra_rama
  rama2
* master
```
En donde se encuentra el "*" 
