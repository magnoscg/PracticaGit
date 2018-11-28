**Paso 11:** Usé el comando `git reset --hard HEAD~1` (reset HEAD~1) para moverme 
al commit anterior y el modificador hard para modificar mi working copy al 
estado del commit anterior.

**Paso 12:** Usé el comando `git reflog` para ver el hash del commit inalcanzable 
que deshice y usé `git reset --hard` + *hash del commit* para volver al commit y
modificar mi working copy tal cual estaba en ese commit.

**Paso 13:** No se puede hacer un merge a **master** porque ya tiene la rama 
**styled** absorbido el commit de **master**. *Already up to date*

**Paso 19:** Causó un conflicto al absorber styled a htmlify porque en las dos
ramas hemos modificado el mismo archivo en las mismas lineas. Git nos marca
las lineas donde hay conflicto para solucionarlo.   

**Paso 21:** No causó ningun conflicto porque la rama styled ya contenia a master.
Simplemente se movio la rama master al commit de la rama de styled. Hicimos un
merge fast-forward.

**Paso 25:** Usé `git log --graph` para dibujar el diagrama con el log.

**Paso 26:** Si podria ser fast-forward porque title tenia los mismo commits que
master más el suyo. Simplemente master avanzo hasta su commit absorbiendo ese
commit. 

**Paso 27:** Usé `git reset HEAD~1` para volver al commit anterior a master sin 
perder los cambios del working copy.

**Paso 28:** Usé `git checkout -- git-nuestro.md` para descartar los cambios.

**Paso 29:** Usé `git branch -D title` para borrar la rama title.

**Paso 30:** Usé `git reflog` para buscar el commit donde estaba title. Voy a ese 
commit con `git checkout` + hash, vuelvo a crear la rama title con `git branch
title` , me cambio a la rama master con `git checkout master` y hago un merge 
con `git merge title`.

**Paso 32:** Usé `git log` par ver el primer commit y con `git checkout` + el hash
puse el Head apuntando a ese commit.

**Paso 33:** Usé `git checkout master` para volver a master que tiene el titulo del
poema.
