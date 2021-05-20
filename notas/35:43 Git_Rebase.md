### 35/43

# Git Rebase

Para comenzar... Qué es *rebase*?

1. *rebase* **es una mala práctica!** 

2. *Rebase* es una instrucción que nos sirve para reemplazar la historia de nuestro repositorio por una modificada en una rama a parte.

   1. Es decir, si por alguna razon nos equivocaramos y crearamos una rama alterna para resolver *bugs* pero al terminar en lugar de hacer *merge* hicieramos *rebase* todo nuestro historial, las memorias de nuestro repositorio serían reemplazadas.

3. *rebase* **es solo para repositorios locales** porque reescribe la historia de nuestro repositorio... esto en GitHub (remoto/compartido) podría traer una cascada de conflictos y al final terminar dañando la inocuidad de nuestro proyecto.

4. Cambia la historia de donde arranco el branch (rama)

   > normalmente para hacer un bugfix (corrección de errores) creamos una rama de "bugfix" para corregir nuestro código y una vez está completa hacemos un merge de nuestros arreglos a la rama maestra. Esto quiere decir que conservamos intacta la historia de nuestro repositorio, incluyendo aun las memorias de nuestro codigo corrupto que habia generado errores anteriormente.

   Con el *rebase* esto cambia porque la historia se reescribe y solo existe hasta el punto desde el cual se creo la rama del rebase y la historia propia de esa rama de cambios, los otros commits es como si nunca hubiesen pasado.

5. ## Cómo se hace? ##

   1. debemos crear una nueva rama para los cambios

      Ej: $ git branch *cambios*

   2. hacemos checkout a esta rama para aplicar nuestros cambios y/o correcciones.

      $ git checkout *cambios*

      hacemos todos los cambios y obviamente si es el caso hacemos los **adds** necesarios y los **commits** que se necesiten para que todo quede agregado a nuestro branch de cambios para **rebase**.

      $ git add *

      $ git commit -am "blabla bla..."

   3. desde la rama de cambio hacemos el rebase

      $ git rebase "main o master"

      ​							--> el nombre de nuestra rama principal o maestra.

      ![image-20210502124123188](/Users/alvaroberrio/Documents/platzi/GIT/Hyperblog/notas/35:43 Git_Rebase.png)

   4. En el supuesto de que nuestra rama principal tuviese cambios que aun no existen en la rama de  rebase (en este caso "experimento"), cuando hacemos el *rebase* el nos mostrara la siguiente información:

      $ git rebase main

      > *rewinding head to replay your work on top of it...* 
      >
      > *applying name_of_commit1*
      >
      > *applying name_of_commit2*  ...

      Algo como esto, nos indica que inspección previa al *rebase* va a realizar **git** en la cual nos indica que va a regresar al **head** de la rama principal y va a hacer un barrido sobre los cambios que se han realizado; se van a aplicar los cambios de la rama de *rabase* y se va a hacer un *automerge*.

   5. Estos cambios solo quedaran registrados en nuestra rama de *rebase* por tal motivo si hicieramos un *checkout* a nuestro *main* solo veriamos los cambios a los cuales le hemos hecho *commit* desde esa rama. 

   6. Al estar actualizada o resuelta la rama de *rebase* con los ultimos commits del *main* y los ajustes *bugfixes* de esta rama, estamos listos para hacer la parte final de nuestro proceso de *rebase* que será fusionarla desde el *main*. 

      $ git checkout main

      $ git rebase experimento

      

      En este punto es donde las historias se fusionan; el *main* será una fusión de su propia historia hasta que conocio a *experimento* y de ahi en adelante es como si estas dos ramas tuvieran vidas gemelas, no hay diferencias y la vida de *experimento* (branch de rebase) se copio en la vida de *main*. 

      *experimento* copio la vida de *main* y luego inserto sus nuevas memorias en la vida de *main* puede decidir desde donde reemplazar sus memorias por las suyas y lo que conoce de *main*. Tenaz! como para una pelicula de Sci-Fi.

      

      > Esto es un rebase, es una forma de hacer cambios silenciosos en otras ramas y volver a pegar la historia de esa rama a una rama anterior haciendole un rebase.
      >
      > Recordar: primero se le hace un rebase a la rama de cambios y luego rebase a la rama en la cual se quieren agregar los cambios y/o modificaciones --> rama final.

      --> No queda historia

      --> no se sabe quien hizo que, no hay forma de controlar blame si varios usuarios utilizan esta rama.

      --> Puede crear una gran cantidad de conflictos.

      