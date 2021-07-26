### 40/43

# Git Reset & Git Reflog

**Usese SOLO en caso de emergencia!!!**

> ¿Qué pasa cuando todo se rompe y no sabemos qué está pasando? Con `git reset HashDelHEAD` nos devolveremos al estado en que el proyecto funcionaba.
>
> - `git reset --soft HashDelHEAD` te mantiene lo que tengas en staging ahí.
> - `git reset --hard HashDelHEAD` resetea absolutamente todo incluyendo lo que tengas en staging.
>
> ***`git reset` es una mala práctica, no deberías usarlo en ningún momento; debe ser nuestro último recurso.***

Si por alguna razón, todo se dañara y quisiera entender que pasó, hay una forma en la que todo queda grabado, esto se llama: *git reflog*.

Con **git reflog** podremos ver tanto los *hash* de los commits y los *heads* del historico de cada repositorio.

- *hash*: es el id que tiene cada commit.
- *head*: todos los heads que ha tenido nuestro repo, es decir sus mutaciones tienen un punto de reconocimiento, y este punto es *HEAD@{#}*.

