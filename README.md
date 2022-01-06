
# platzi-git
# Readme.md es una excelente práctica
Editor online
https://pandao.github.io/editor.md/en.html

# Tu sitio web público con GitHub Pages
https://pages.github.com/
repositorio publico con el mismo nombre del usuario de github
codigo en index.html
configurar en el repositorio (settings) pages.github
para cargar en la raiz, cambiar el nombre del repositorio (yordayfigueroasanchez.github.io)

# Git Rebase: reorganizando el trabajo realizado
puedes recoger todos los cambios confirmados en una rama y ponerlos sobre otra (mala practica)
    rebase desde la rama particular para traer los cambios de la master
		git rebase master
    rebase desde master para traer los cambios de la rama particular
		git rebase experimento
# Git Stash: Guardar cambios en memoria y recuperarlos después
    git stash : Guarda el trabajo actual de manera temporal. (Archivos modificados o eliminados)
    git stash -u : Crea un stash con todos los archivos. (Añadiendo los creados Untracked)
    git stash save “mensaje” : Crea un stash con el mensaje especificado.
    git stash list : Permite visualizar todos los stash existentes.
    git stash clear : Elimina todos los stash existentes.
    git stash drop : Elimina el stash más reciente. El que tiene num_stash=0.
    git stash drop stash@{num_stash} : Elimina un stash específico.
    git stash apply : Aplica el stash más reciente. El que tiene num_stash=0.
    git stash apply stash@{num_stash} : Aplica los cambios de un stash específico.
    git stash pop : Aplica el stash más reciente y lo elimina. El que tiene num_stash=0.
    git stash pop stash@{num_stash} : Aplica los cambios de un stash específico y elimina lo stash.
    git stash branch nombre_de_rama : Crea una rama y aplica el stash mas reciente.
    git stash branch nombre_de_rama stash@{num_stash} : Crea una rama y aplica el stash especificado.
# Git Clean: limpiar tu proyecto de archivos no deseados
	git clean --dry-run (vista previa)
 	git clean -f
	git clean -df hubiera borrado la carpeta “css - copia”
# Git cherry-pick: traer commits viejos al head de un branch
	desde la rama donde llegara el commit
	git cherry-pick <numero del commit>
# Reconstruir commits en Git con amend
despues de hacer el commit nos percatamos que falta algo mas
--amend
	git add 
	git commit --amend
# Git Reset y Reflog: úsese en caso de emergencia
reset reflog (mala practica)
resetea al identificador que tomemos de (git reflog)
git reset --soft "hash del commit"
git reset --hard "hash del commit"
# Buscar en archivos y commits de Git con Grep y log
	git grep -n color (numero de linea donde aparece la palabra color)
	git grep -c color (contar las apariciones de la palabra color)
	git log -S "cabeza" (buscar en commit)
# Comandos y recursos colaborativos en Git y GitHub
	git shortlog -sn = muestra cuantos commit han hecho cada miembros del equipo.
	git shortlog -sn --all = muestra cuantos commit han hecho cada miembros del equipo hasta los que han sido eliminado
	git shortlog -sn --all --no-merge = muestra cuantos commit han hecho cada miembros quitando los eliminados sin los merges
 	git blame ARCHIVO = muestra quien hizo cada cosa linea por linea
 	git COMANDO --help = muestra como funciona el comando.
 	git blame history.txt -L35,50= muestra quien hizo cada cosa linea por linea indicándole desde que linea ver ejemplo -L35,50
	git branch -r **= se muestran todas las ramas remotas
	git branch -a = se muestran todas las ramas tanto locales como remotas