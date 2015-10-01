# Tutorial de Git en Español
Comandos fundamentales para comenzar a trabajar con Git. Este tutorial asume de que ya se tiene un proyecto en Git, por lo que omitirá la iniciación o clonación de un proyecto existente.
#Comandos básicos
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
Si queremos saber en cuál rama nos encontramos, para saber donde subir nuestros cambios, debemos escribir el siguiente comando:
```
git branch
```
Una vez escrito el comando anterior, visualizaremos algo parecido a lo siguiente:
```
  otra_rama
  rama2
* master
```
El "*" indica en cuál rama nos encontramos, en el caso del ejemplo, estamos en la rama "master".
Si quisieramos cambiar de rama, debemos escribir el siguiente código:
```
git checkout nombre-rama
```
En base a las ramas listadas en el ejemplo anterior, el comando sería de la siguiente manera:
```
git checkout rama2
```
Si tenemos otro colaborador en nuestro proyecto y queremos obtener los cambios que el a envíado a la rama remota, debemos escribir el siguiente código:
```
git pull origin master
```
Para el ejemplo anterior se asumió que se está trabajando sobre la rama master.
#Comandos útiles
