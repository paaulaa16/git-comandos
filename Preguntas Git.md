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