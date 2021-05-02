### 35/43

# Git Rebase

Para comenzar... Qué es *rebase*?

1. *rebase* **es una mala práctica!** 

2. *Rebase* es una instrucción que nos sirve para reemplazar la historia de nuestro repositorio por una modificada en una rama a parte.

   1. Es decir, si por alguna razon nos equivocaramos y crearamos una rama alterna para resolver *bugs* pero al terminar en lugar de hacer *merge* hicieramos *rebase* todo nuestro historial, las memorias del nuestro repositorio serían reemplazadas.

3. *rebase* **es solo para repositorios locales** porque reescribe la historia de nuestro repositorio... esto en GitHub (remoto/compartido) podría traer una cascada de conflictos y al final terminar dañando la inocuidad de nuestro proyecto.

4. Cambia la historia de donde arranco el branch (rama)

   > normalmente para hacer un bugfix (corrección de errores) creamos una rama de "bugfix" para corregir nuestro código y una vez está completa hacemos un merge de nuestros arreglos a la rama maestra. Esto quiere decir que conservamos intacta la historia de nuestro repositorio, incluyendo aun las memorias de nuestro codigo corrupto que habia generado errores anteriormente.

   Con el *rebase* esto cambia porque la historia se reescribe y solo existe desde que se creo la rama desde la cual se hace el rebase, los otros commits es como si nunca hubiesen pasado.

5. 