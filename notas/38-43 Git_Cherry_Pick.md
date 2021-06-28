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

Esto nos indica que la nueva rama nos deja en un punto como si estuvieramos desde el main pendiente de agregar al Staging los cambios realizados y copiados al stash.

