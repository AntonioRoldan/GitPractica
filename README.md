**¿Qué comando utilizaste en el paso 11? ¿Por qué?**

git reset —hard HEAD~1 

Para desplazar el puntero styled al commit anterior usando --hard para recuperar el working copy de ese commit deshaciendo mis cambios recientes. 

**¿Que comando o comandos utilizaste en el paso 12? ¿Por qué?**

git reflog, git reset <ID de commit> y git checkout -- git-nuestro.md 

Git reflog para encontrar el ID del siguiente commit que he deshecho, git reset para mover el puntero styled allí y git checkout -- git-nuestro.md para recuperar los cambios. Aunque git reset --hard <ID de commit> también habría valido. 


**El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?**

No se causó conflicto porque el archivo git-nuestro.md no fue modificado desde master.

**El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?**

Si porque htmlify modifica el archivo en las mismas líneas que modifiqué desde styled.

**El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?**

No porque desde master no hice ninguna modificación a git-nuestro.md, habrían aparecido conflictos si hubiera añadido un cambio en alguna linea pero no si hubiera añadido una nueva línea. 

**¿Qué comando o comandos utilizaste en el paso 25?** 

Git log --graph --decorate 

**El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?** 

No porque no se crearon nuevos commits en la rama master. Los merge no fast-forward son para no perder cambios que se hayan hecho en la rama desde la que hacemos merge porque un fast forward mueve el puntero de la rama desde la que se hace merge hasta el último commit de la rama que se absorbe. 

**¿Que comando o comandos utilizaste en el paso 27?** 

git reset HEAD~1 

Para mover el puntero master al commit anterior sin deshacer cambios como ocurriría si hubiera usado git reset --hard HEAD~1 

**¿Que comando o comandos utilizaste en el paso 28?** 

git checkout -- git-nuestro.md 

Para deshacer los cambios hechos a git-nuestro al hacer el merge 


**¿Que comando o comandos utilizaste en el paso 29?** 

git branch -D title 

Usando -D me salto los warnings que salen al borrar una rama con -d 


**¿Que comando o comandos utilizaste en el paso 30?** 

git reflog, git reset <ID de commit>, git checkout -- git-nuestro.md 

Con git reflog localizo el ID del commit que se creó al hacer el merge, git reset <ID de commit> me lleva allí y con git checkout -- git-nuestro.md recupero los cambios del merge aunque git reset --hard <ID de commit> habría valido también. 


**¿Que comando o comandos utilizaste en el paso 32?** 

git reflog y git reset <ID de commit> 

Con git reflog puedo ver los IDs de cada commit para luego moverme a ellos con reset para no quedarme en detached HEAD sin deshacer cambios  


**¿Que comando o comandos utilizaste en el paso 33?** 

git reflog y git reset <ID de commit> 

Con git reflog busco el commit con mensaje "Añado titulo a git-nuestro.md desde title" y con reset muevo el puntero de la rama master a ese commit 
