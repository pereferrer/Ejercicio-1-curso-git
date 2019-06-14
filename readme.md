# Ejercicio 1

# - ¿Qué comando utilizaste en el paso 11? ¿Por qué?

<p>He utilizado el comando git reset --hard HEAD~1, git reset HEAD~1 solo nos devolvería
al commit padre(anterior) pero mantendría los cambios realizados en el working copy por lo
que los cambios realizados en git-nuestro.md seguirían presentes. Sin embargo,
añadiendo la opción --hard al comando anterior le indicamos que los cambios en el working copy
también vuelvan al estado anterior por lo que tendremos la versión original del fichero.</p>

# - ¿Qué comando o comandos utilizaste en el paso 12? ¿Por qué?

<p>El primer comando utilizado ha sido git reflog para obtener el identificador del commit al que volvemos volver. 
Acto seguido, he ejecutado git reset --hard fe6ab76 para deshacer el 
commit y que realice también los cambios en el working copy. Finalmente, verifico en que 
commit se encuentra la rama y verifico que el contenido del fichero es el correcto. 
También podemos verificar en que commit nos encontramos con git log.</p>


# - El merge del paso 13, ¿Causó algún conflicto? ¿Por qué?

<p>El merge del paso 13 no causa conflicto debido a que la rama Styled se creó después de la 
primera edición de git-nuestro.md y posteriormente no se han realizado más cambios en el 
fichero git-nuestro.md en la rama master por lo que no tiene nada que absorber nuevo en la rama Styled.</p>


# - El merge del paso 19, ¿Causó algún conflicto? ¿Por qué? 

<p>Si ha causado conflicto, debido a que ambos ficheros han sido modificados desde el commit 
inicial y hay que decidir qué cambios queremos mantener y cuales descartar para resolver el conflicto.</p>


# - El merge del paso 21, ¿Causó algún conflicto? ¿Por qué? 

<p>No causó conflicto porque ambas ramas forman una lista. Entonces en este caso el puntero 
de la rama master solo tiene que actualizarse para que apunte al puntero del último commit 
de la rama Styled y así los commits de la rama Styled pasan a estar visibles para la rama Master.</p>


# - ¿Qué comando o comandos utilizaste en el paso 25?

<p>He utilizado el comando git log --graph, también podemos usar git log --graph --decorate --pretty=oneline. 
Asimismo, podría haber creado un alias para las siguientes ejecuciones con git config alias.graph "log --graph --decorate --pretty=oneline" 
y luego solo tener que ejecutar git graph.</p>

# - El merge del paso 26, ¿Podría ser fast forward? ¿Por qué? 

<p>No, porque en este caso afectaría a la rama Styled debido a que el puntero de Master 
apuntaba al último commit de la rama Styled al haberla absorbido con un merge fast forward.</p>

# - ¿Qué comando o comandos utilizaste en el paso 27?

<p>He utilizado git reset HEAD~1 para volver al commit anterior sin la opción --HARD. Con la opción hard no se hubiera mantenido el working copy.</p>


# - ¿Qué comando o comandos utilizaste en el paso 28? 

<p>Para descartar los cambios del archivo git-nuestro.md ejecutamos el comando git checkout git-nuestro.md</p>

# - ¿Qué comando o comandos utilizaste en el paso 29? 

<p>Para eliminar la rama title ejecutamos: git branch -D title </p>

# - ¿Qué comando o comandos utilizaste en el paso 30? 

<p>Primero con git reflog debemos buscar el identificador del commit en el cual habíamos hecho el merge con la rama title. 
Posteriormente, ejecutamos git reset --hard 3314b8b para rehacer el merge.</p>

# - ¿Qué comando o comandos usaste en el paso 32?

<p>Primero debemos ejecutar git reflog para buscar el identificador del primer commit. 
Acto seguido, ejecutamos git-reset 14b004f para volver al commit inicial manteniendo los cambios en el working copy.</p>

# - ¿Qué comando o comandos usaste en el punto 33?

<p>He utilizado los mismos comandos que el paso anterior. Git reflog para obtener el 
identificador del commit con el estado final, cuando pusimos título al poema. 
Finalmente, ejecutamos git reset 3314b8b. En esta ocasión la opción --hard tampoco nos hace falta porque ya teníamos la última versión en el working copy.</p>
