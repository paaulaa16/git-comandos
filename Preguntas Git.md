# PREGUNTAS GIT
**1- ¿Como puedo deshacer  el ultimo commit en Git?**
~~~ 
git reset [--mixed] HEAD~1 
~~~

**2- ¿Como cambiar el mensaje de un commit?**
~~~
git commit --amend -m "Este es el nuevo comentario"
~~~

**3- ¿Como puedo renombrar una rama en Git?**
~~~
git branch -m <nombre_viejo> <nombre_nuevo>
~~~

**4- ¿Como borrar una rama remota que no existe en el servidor?**
~~~
git push origin :rama_remota
~~~

**5- ¿Que diferencia hay entre 'git rebase' y 'git merge'?**
~~~
git-rebase
~~~
- Genera una serie de commits secuencialmente, de modo que puedan aplicarse directamente sobre la cabeza del nodo.

~~~
git-merge
~~~
- Une dos o más historiales de desarrollo.

**6- ¿Como ver que archivos son diferentes entre 2 ramas con Git?**
~~~
$ git diff branch1..branch2
~~~

**7- ¿Como consultar en git los commits en los que se modificó un archivo?**
~~~
git log --follow -- nombreArchivo
~~~
- Los **--** antes de **nombreArchivo** sirven para indicar explícitamente que **nombreArchivo** corresponde a un archivo (y no, por ejemplo, al nombre de una rama).

**8- ¿Como crear mi propio servidor de Git?**
~~~
git clone user@ip_servidor:/var/www/html/carpeta_del_proyecto/repositorio.git
~~~

**9- ¿Como averiguar la procedencia de una rama determinada?**
Haces un checkout a la rama en cuestion y luego ejecuta:
~~~
git log --oneline --decorate --all --graph
~~~

**10- ¿Cual es la diferencia entre commit y push en Git?**

**Git push** trabaja a nivel de repositorio remoto, mientras que **git commit** trabaja en tu repositorio local.

![imagen](https://manuais.iessanclemente.net/images/4/4b/File-Status-Git.png)

**11- ¿Cuál es la diferencia entre “git rm --cached” y “git reset HEAD”?**

Las diferencias son las siguientes:

**- git rm -cached <file>**: remueve el archivo del indice, esto quiere decir, que Git ya no le hará seguimiento. Aunque el archivo seguirá existiendo en tu directorio, tal y como está.
  
**-git reset HEAD <file>**: devuelve el archivo a su último commit y este sigue en seguimiento por git, es decir podras hacer add, commit, etc.
