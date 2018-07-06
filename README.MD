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

## Ver el historial de commits (Se agrega decoraciones)

- `--oneline` Describe que solo mostrara en una linea el titulo del commit y el los primeros digitos del HADH
- `--decorate` Muestra la posicion del HEAD y ramas

> `git log --oneline --decorate` 
> 
> ![](https://github.com/OneSevenDev/OnlyGit/blob/master/resources/gitlogonelinedecorate.png?raw=true)

## Revertir cambios

Por cada rever se genera un commit nuevo

> `git revert HEAD` : revierte el commit actual
> 
> `git revert HEAD~1` : revierte un commit atras al actual

Si se desea revertir varios cambios, se recomienda seguir el flujo regresando atras de uno en uno, de no usar de esta forma, puede generar conflictos y toca resolverlos de manera manual. Al hacer esta forma solo se genera un solo commit.

> `git revert --no-commit HEAD`
> 
> `git revert --no-commit HEAD~1`
> 
> `git revert --no-commit HEAD~2`
> 
> `git revert --no-commit HEAD~3`

Para confirmar todos los commit a revertir

> `git revert --continue`

Para retornar al commit inicial y desacer la reversion

> `git revert --abort`

## Comparar commits

Se puede usar HEAD (commit actual) o el HASH del commit

> `git diff HEAD~3 HEAD~4`
> 
> ![](https://github.com/OneSevenDev/OnlyGit/blob/master/resources/diff_heads.png?raw=true)
> 
> `git diff 2457f99 99d5fc0`
> 
> ![](https://github.com/OneSevenDev/OnlyGit/blob/master/resources/diff_hash_commit.png?raw=true)

## Mostrar flujo graficado en la terminal del historial de Git

> `git log --oneline --decorate --all --graph`
> 
> ![](https://github.com/OneSevenDev/OnlyGit/blob/master/resources/gitlogonelinedecorategraph.png?raw=true)

## Crear, Listar y eliminar alias


> `git config --global alias.unstage 'reset HEAD --'`
> 
> ![](https://github.com/OneSevenDev/OnlyGit/blob/master/resources/git_unstage.png?raw=true)
> 
> Listar unicamente los alias
> 
> `git config --global --get-regexp alias`
> 
> Listar los cambios definidos por el usuario, incluye los alias
> 
> `git config --global -l`
> 
> Eliminar un alias
> 
> `git config --global --unset alias.unstage`