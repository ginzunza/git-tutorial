# Tutorial de Git en Español
Comandos fundamentales para comenzar a trabajar con Git. Este tutorial asume de que ya se tiene un proyecto en Git, por lo que se ha omitido la iniciación o clonación de un proyecto existente.
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
Si tenemos otro colaborador en nuestro proyecto y queremos obtener los cambios que él a envíado a la rama remota, debemos escribir el siguiente código:
```
git pull origin master
```
Para el ejemplo anterior se asumió que se está trabajando sobre la rama master.
#Comandos útiles
1.- Observar todos los commit que se han hecho en una rama:
```
git log

#el output será algo así:
commit 48ead24ab3c3c940736ecf65064019b5a790619b
Author: Gustavo <ginzunza@rebuss.cl>
Date:   Thu Oct 1 15:47:03 2015 -0300

    cambios

commit d49f5b83e5b15a5b73573772c6c3ba89907d2ebe
Author: Gustavo <ginzunza@rebuss.cl>
Date:   Thu Oct 1 15:02:14 2015 -0300

    dynamic select

commit 7ba3a7beca6f07b04aa1c0e0136b106fab6159c1
Author: Gustavo <ginzunza@rebuss.cl>
Date:   Wed Sep 30 18:20:24 2015 -0300

    trying to add a dynamic select to companies
```
Para dejar de visualizar los logs se debe presionar la letra "q".
Si queremos observar cómo se veía nuestro proyecto en cierto commit, sin hacer los cambios de manera definitiva. Debemos escribir el siguiente comando:
```
git checkout 48ead24ab3c3c940736ecf65064019b5a790619b
```
El código del checkout fue sacado del primer output del "git log" anterior. El checkout nos generará una rama temporal, en donde podremos visualizar cómo era nuestro proyecto en el commit seleccionado. Para volver a nuestra rama, sin guardar ningún cambio, basta con escribir:
```
git checkout nombre-rama
```
2.- Descartar cambios sin commit y eliminar archivos agregados al proyecto sin commitear<br/>
Para descartar cambios que no queremos unir al proyecto, mediante commit, debemos escribir el siguiente código:
```
git stash
```
Para eliminar todos los archivos que se han agregado al proyecto, pero que no han sido commiteados:
```
git clean -f -d
```
