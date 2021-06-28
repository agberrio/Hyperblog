### 39/43

# Git Amend

**Reconstruír Commits en Git con Amend**

________________

> A veces hacemos un commit, pero resulta que no queríamos mandarlo porque faltaba algo más. Utilizamos `git commit --amend`, *amend* en inglés es remendar y lo que hará es que los cambios que hicimos nos los agregará al commit anterior.

## Ejemplo

> vamos a realizar dos cambiosque teniamos programados para nuestro proyecto:
>
> 1. Cambiar el nombre del blog ne *post.html*
>
> 2. Cambiar el color del Footer
>
> Estos dos cambios deberán quedar en el mismo commit!
>
> Pero que pasa si yo hice un solo cambio y en el momento de hacer el commit le puse la descripción de los dos cambios???
>
> Puedo enmendar esto???, tranquilo! para eso esta *amend*

1. realice el primer cambio

2. $ git status

3. $ git commit -am "hice los dos cambios"

4. Recuerdo que la cagué porque solo hice uno de los dos cambios

5. hago el segundo cambio

6. y ahora intentare fusionar mis dos cambios.

7. $ git add {ruta del archivo cambiado}

   > Cuando cometemos estos errores es necesario hacer el add, para poderlo agregar al commit realziado

8. $ git commit --amend

   > Con esto le estamos diciendo a Git que los cambios que hicimos los queremos agregar al commit inmediatamente anterior.
   >
   > Git nos abrira una instancia en VIM para poder editar el mensaje del commit y confirmar el cambio.

9. 