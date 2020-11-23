# Ejercicio 1

## ¿Qué comando utilizaste en el paso 11? ¿Por qué?

**git reset --hard HEAD~1** Porque lo que hago para descartar los cambios en la rama *styled* es mover el puntero *HEAD* y *styled* al commit anterior con **git reset HEAD~1** y añadiendo **--hard** hago que my *Working Copy* quede como antes de haber realizado esos cambios del commit que he querido deshacer.


## ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

**git reflog** para encontrar ese commit que quedó descartado. Encuentro que su id es 0bfdfb1.  
**git reset --hard 0bfdfb1** para mover la rama *styled* y el puntero *HEAD* a ese commit. Con **--hard** recupero ese trabajo en mi *Working Copy*.


## El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

**git merge master** No causa conflicto alguno porque es un merge sin bifurcaciones y sin commit, es decir, un merge *fast forward*. Si *styled* absorbe a *master* estando así https://imgur.com/a/tk2TmAq realmente es como no hacer nada. Es un paso un poco trampa ya que no se mueve ningún puntero.


## El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

Si, porque varias lineas del mismo archivo contienen cambios distintos.


## El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

No, porque es un merge *fast forward* sin bifurcacion y sin commit. Solo he movido el puntero *master* al commit donde esta el puntero *styled*.


## ¿Qué comando o comandos utilizaste en el paso 25?

**git config --global alias.graph "log --graph --oneline"** Me dejo configurado para mas tarde un alias.  
**git graph** Pinto en la consola el grafo.


## El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

Sí podría. Porque entre title y master no hay bifurcaciones, están el lista y podría hacer merge *fast forward* que sería equivalente a mover con **git reset** el puntero *title* al commit donde está el puntero *master*.


## ¿Qué comando o comandos utilizaste en el paso 27?

**git reset HEAD~1**


## ¿Qué comando o comandos utilizaste en el paso 28?

**git checkout -- git-nuestro.md** estoy en la versión antigua. En la nueva sería **git restore --staged git-nuestro.md**.  
El paso anterior y este se podrían hacer en un solo paso: **git reset --hard HEAD~1** para deshacer el merge descartando los cambios en mi *Working Copy*.

## ¿Qué comando o comandos utilizaste en el paso 29?

**git branch -D title**


## ¿Qué comando o comandos utilizaste en el paso 30?

**git reflog**  
**git reset --hard a948c88**


## ¿Qué comando o comandos usaste en el paso 32?

**git log**  
**git reset --hard 067ec08c8cee2009f0c14ced5361fbcb99184be7**


## ¿Qué comando o comandos usaste en el punto 33?

**git reset --hard a948c8877940f9706225e33ac92035ddf9ed5da0**
