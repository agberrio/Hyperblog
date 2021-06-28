### 38/43

# Git Cherry Pick

**Traer commits viejos al head de un branch**

______

> "Existe un mundo alternativo en el cual vamos avanzando en una rama pero necesitamos en *master* uno de esos avances de la rama, para eso utilizamos el comando `git cherry-pick IDCommit`.
>
> *cherry-pick es una mala práctica* porque significa que estamos reconstruyendo la historia, **usa cherry-pick con sabiduría**. Si no sabes lo que estás haciendo **ten mucho cuidado**."

## EJEMPLO:

Si yo realizó un cambio en un documento de mi rama maestra/main podría hacer un *stash* de estos cambios y agregarlos como el contenido de una nueva rama como vimos en el campitulo de *stash*

$ git stash --> para guardar los cambios temporalmente en stash

$ git stash branch {nombre de la nueva rama}

​	>>para agregar nuestros cambios guardados en el *stash* en una nueva rama.

Una vez tenemos nuestra nueva rama, si hicieramos un "git status" nos dariamos cuenta que los cambios estan si agregar, por lo cual debemos hacer un "commit -am"

$ git status

$ git commit -am "mensaje de los cambios"

Esto nos indica que la nueva rama nos deja en un punto como si estuviéramos desde el main pendiente de agregar al Staging los cambios realizados y copiados al stash.

Si hacemos nuevos commits a esta rama, recordemos que estos serán exclusivos solo para esta rama... es decir, nuestra rama main y nuestra nueva rama se diferenciarna aun mas... y es aqui, donde *cherry pick* podrá cumplir su funciona super espectacular!!!!

Si estuvieramos 3 o 4 o muchos commits avanzados en esta "nueva rama", pero que no forman parte de head del main de nuestro proyecto; si fuese necesario podriamos seleccionar uno de estos commits en "nueva rama" para incorporarlos a nuestro proyecto en la rama main. 

Desde "nueva rama":

$ git log --oneline

> para ver el id del commit que quiero llevar al main

una vez he copiado el id del commit, vuelvo al main

$ git checkout main

Y agrego el commit a mi head main

$ git cherry-pick [id_commit]

Listo, ya tenemos nuestro cambio incorporado al main!!

> *cherry-pick es una mala práctica* porque significa que estamos reconstruyendo la historia, **usa cherry-pick con sabiduría**. Si no sabes lo que estás haciendo **ten mucho cuidado**."

Si revisamos el log, podremos ver que todos los cambios que agregamos quedan en el registro comosi hubieran sido realizados en la rama sobre la cual se migraron los cambios; es decir para este caso, como si estos cambios hubiesen sido realizados desde el main. y esto no es cierto... por eso hay que tener mucho cuidado con este comando.... con responsabilidad y conocimiento de causa.... si la embarras. Git te permite corregir todo y dejarlo como lo tenias antes... esa es la magia de git!

