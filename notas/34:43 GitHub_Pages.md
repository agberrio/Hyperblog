### 34/43

# GitHub Pages

**GitHub** tiene un servicio de Hosting gratuito, llamado **GitHub Pages**. Donde pordremos tener todo el contenido de nuestros repositorios pero como si fueran una pagina Web. Es decir... público para todo el mundo

**pages.github.com**

## 1. Para crear nuestro sitio en Pages de GitHub, debemos desde nuestra cuenta de GitHub crear un repositorio con el nombre de nuestra cuenta.

> Ej: si tu nombre de usuario es "logos" --> entonces debes crear un repositorio así
>
> ​		logos.github.io

## 2. Clonar tu nuevo repositorio.github.io desde la terminal de tu Git (repo local)

​		$ git clone (https/ssh).git

## 3. Ahora debemos crear nuestro índex.html

​		$ vim index.html

​						o

​		$ code index.html					o					$ atom index.html

​		Hay multiples opciones para hacer este paso, lo importante es con cual editor de texto te sientes mejor crando este 		archivo.

Una vez que has diseñado tu índex.html pordras continuar al siguiente paso.

## 4. push it!

​		Como siempre cada vez que generamos nuevo contenido o modificamos nuestros archivos trackeados por git debemos agregarlos al repositorio.

​	$ git status

​	$ git add --all	$ git add *	$ git add index.html

​	$ git commit -am "mensaje"

​	$ git pull origin master

​	$ git push origin master

## 5. Listos, puedes entrar...

​	logos.github.io



![image-20210430112909642](/Users/alvaroberrio/Library/Application Support/typora-user-images/image-20210430112909642.png)