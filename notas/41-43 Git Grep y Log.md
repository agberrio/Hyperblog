### 41/43

# Git Grep & Git Log

**Buscar en archivos y commit con *grep* y *log***

> A medida que nuestro proyecto se hace grande vamos a querer buscar ciertas cosas.
>
> Por ejemplo: ¿cuántas veces en nuestro proyecto utilizamos la palabra *color*?
>
> Para buscar utilizamos el comando `git grep color` y nos buscará en todo el proyecto los archivos en donde está la palabra *color*.
>
> - Con `git grep -n color` nos saldrá un output el cual nos dirá en qué línea está lo que estamos buscando.
> - Con `git grep -c color` nos saldrá un output el cual nos dirá cuántas veces se repite esa palabra y en qué archivo.
> - Si queremos buscar cuántas veces utilizamos un atributo de HTML lo hacemos con `git grep -c "<p>"`.

$ git log -S "palabra o caracter de búsqueda" --> esto busca una palabra cuantas veces fué usada dentro de los commits.

Grep --> para los archivos

Log --> para los commits





