# Ejercicio 1

## Repuestas

- ¿Qué comando utilizaste en el paso 11? ¿Por qué?

    ~ Para el paso 11 utilicé el comando 
    `git reset --hard 5134fa7` siendo "5134fa7" el id del commit. Para ello antes realicé un `git reflog` para sacar el Id del commit. 
    Realicé esto ya que se pedía deshacer el último commit perdiendo los cambios realizados en el working copy y este comando me permite volver l comit que se requiere y descartar los cambios en un mismo paso. 
    También podría haberlo hecho en 2 pasos haciendo `git reset HEAD~1` y luego `git restore git-nuestro.md`.

- ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

    ~ Al igual que en el caso anterior realicé el mismo comando `git reset --hard b7e938b` siendo "b7e938b" el id del commit. Para ello nuevamente realicé un `git reflog` para sacar el Id del commit. Hago esto ya que estamos queriendo rehacer el ultimo commit el que acabamos de deshacer, por lo que se requiere hacer lo mismo que anteriormente solo que volviendo al commit anterior con los cambios que tenía.
    También al igual que el caso anterior podría haberlo hecho en 2 pasos haciendo `git reset b7e938b` y luego `git restore git-nuestro.md`.
    
    La diferencia aquí sería que en este caso es de vital importancia el comando `git reflog` ya que en el paso 11 no hubiera sido necesario si quisieramos consultar el id del commit ya que podríamos volver al commit padre con el comando `git reset HEAD~1`, pero en el paso 12 sin el comando `git reflog` no podría haber vuelto atras, ya que ahora estaba en el commit padre y este no ve al hijo. Por esa razon tanto para hacerlo en 1 paso o en 2 se necesita de este Id.

- El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

    ~ En el merge del paso 13 no tuve ningun conflicto. 
    Esto es correcto, ya que se pidió que *styled* absorba a *main*, esto quiere decir que los cambios de *main* se pasaron a *styled*. Pero como styled fue creada a partir de *main* y en *main* no hubo ninguna otra modificación esos cambios ya estaban en la rama *styled*, de hecho, git me dio un mensaje diciendo esto mismo `Already up to date`.

- El merge del paso 19, ¿Causó algún conflicto? ¿Por qué?

    ~ El merge del paso 19, en cambio, si me dio conflictos y también es correcto, ya que se pedía realizar un merge de la branch *htmlfy* a la *styled*, es decir, que *styled* absorba a *htmlfy*. A diferencia del merge anterior la branch *htmlfy* no se creo a partir de *styled*, las dos fueron creadas desde *main* y las dos tenían commits con modificaciones al contenido de la branch *main* en las mismas lineas.

- El merge del paso 21, ¿Causó algún conflicto? ¿Por qué?

    ~ Este merge no causó ningun conflicto, ya que se pidió que *main* absorba a *styled*, esto quiere decir que los cambios de *styled* se pasaron a *main*. Pero como *styled* fue creada a partir de *main* y en *main* no hubo ninguna otra modificación esos cambios ya estaban en la rama *styled*. Solamente se pasaron los nuevos cambios hechos en *styled* a *main* y ahora las dos ramas i contienen lo mismo.

- ¿Qué comando o comandos utilizaste en el paso 25?

    ~ Utilicé el comando `git log --graph --oneline`

- El merge del paso 26, ¿Podría ser fast forward? ¿Por qué?

    ~ El merge del paso 26 podría haber sido tranquilamente "fast forward", ya que al igual que en el merge del paso 21 la branch *title* fue creada desde *main*, esta no tuvo ningun cambio y podría simplemente pasar los commits de *title* a main de esta manera sin crear un nuevo commit con el merge como lo hicimos de la manera no "fast forward"

- ¿Qué comando o comandos utilizaste en el paso 27?

    ~ Utilicé el comando `git reset HEAD~1`.

- ¿Qué comando o comandos utilizaste en el paso 28?

    ~ Utilicé el comando `git restore git-nuestro.md`.

- ¿Qué comando o comandos utilizaste en el paso 29?

    ~ Utilicé el comando `git branch -D title`.

- ¿Qué comando o comandos utilizaste en el paso 30?

    ~ Primero realicé un `git reflog` para sacar el id del commit("c89aeca") del merge al que quería volver y luego utilicé el comando `git reset --hard c89aeca`.

- ¿Qué comando o comandos usaste en el paso 32?

    ~ Al igual que el paso 30 primero realicé un `git reflog` para sacar el id del commit inicial("5134fa7") del merge al que quería volver y luego utilicé el comando `git reset --hard 5134fa7`.

- ¿Qué comando o comandos usaste en el punto 33?

    ~ Y aquí lo mismo que la respuesta anterior primero el `git reflog` para sacar el id del commit cuando pusimos el titulo al poema("c89aeca") y luego utilicé el comando `git reset --hard c89aeca`.
