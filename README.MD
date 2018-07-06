# Ayuda de comandos

## Agregar Archivos del *Directorio de trabajo* al *Staging Area*

> `git add <path_file>`
> 
> `git add .`

## Confirmar cambios en *Staging Area*

> Usando *Nano* (Editor de textos en la terminal)
> 
> `git commit` 
> 
> `git commit -m 'Descripcion de los cambios'`

## Retornando del Staging Area al Directorio de Trabajo

> `git reset HEAD <path_file>` 
> 
> `git reset HEAD .`

## Eliminando completamente commit

> `git reset --hard <hash_commit>` 
> 
> Elimina completamente el último commit
> 
> `git reset --hard HEAD~1 .`