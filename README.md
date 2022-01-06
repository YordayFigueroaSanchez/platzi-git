
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