### 37/43

# Git Clean

**Limpiar proyectos de archivos no deseados**

__________________

A veces creamos archivos cuando estamos realizando nuestro proyecto que realmente no forman parte de nuestro directorio de trabajo, que no se deberían agregar y lo sabemos.

- Para saber qué archivos vamos a borrar tecleamos `git clean --dry-run`
- Para borrar todos los archivos listados (que no son carpetas) tecleamos `git clean -f`

Git sabe cual es la estructura de nuestro repositorio, sobre el cual estamos trabajando 

**Nota:** 

1. Git Clean no limpia los tipos de archivos especificados en nuestro archivo de exclusiones *.gitignore*

2. Git Clean no limpia carpetas de archivos, solo archivos. Es decir si nosotros duplicamos una carpeta, Git Clean no va a borrar los archivos que lo contienen porque lo unico que cambia el nombre es la carpeta pero no su contenido, y como esos archivos con esas extensiones estan en seguimiento dentro del repositorio, estos no serán eliminados.

