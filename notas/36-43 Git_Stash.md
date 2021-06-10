### 36/43

# Git Stash

### Guardar cambios en memoria y recuperarlos despues

__________

* Recordemos:

  $ gitk

  ​	-> es un comando que nos permite abrir el log de nuestro repositorio en modo visual de git

  _____________

Aclaración: Cuando estamos en cualquier rama dentro de nuestro repositorio y realizamos cambios, estos debemos agregarlos a nuestro historial de cambios haciendoles un *commit* y un *add* si fuese necesario (en el caso de que nuestro cambio incluya un nuevo archivo que no estaba en seguimiento). **Si estos cambios no los agregamos con un *commit* los podremos perder**.

:arrow_right: pero puede pasar que los cambios que realicemos nos los queramos *comitear* inmediatamente, o los queremos desechar por completo aunque los archivos hubiesen sido salvados localmente. para este tipo de casos existe **Git Stash**.

**Stashed:Estashear**: Guardar cambios para decidir que hacer con ellos después.

**Git Stash** es una lista de estados que nos guarda algunos cambios en *staging* que no han sido *comiteados*, sin que los perdamos y los podamos agregar o desechar posteriormente.

Esto es útil, en casos en los que se daña nuestra rama pero los cambios no han sido *comiteados* podremos sacar los errores y desecharlos. 

Tambien cuando hemos avanzado en una rama pero necesitamos recuperar alguna información de otra rama para agregarla a los cambios actuales pero no queremos perder nuestro progreso, es alli donde *stash* brilla; pues podremos guardar nuestros cambios sin perderlos, volver a la rama de la cual queremos sacar información, agregarla a la rama principal y finalmente volver a agregar nuesto *stash* a los cambios para *commit*.



$ git stash

$ git stash list

$ git stash pop

$ git stash drop

$git stash branch [branch_name]











