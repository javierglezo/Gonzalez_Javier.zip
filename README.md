# Gonzalez_Javier.zip

NOMBRE: Javier González
LINK: https://github.com/javierglezo/Gonzalez_Javier.zip  

RESPUESTAS EXAMEN:
1. Un pull request es la acción final de mandarle tus cambios de un repositorio al propietario de ese mismo repositorio que podrá aceptarlos o no. Ej. Hago un fork de su repositorio, me lo clono en local, realizo cambios, los subo con "git push" a mi copia de su repositorio y una vez tengo eso, desde su repositorio puedo mandarle una propuesta y así podrá integrar mis cambios (**pull request**)

2. Un merge conflict es un conflicto de ramas al intentar integrar una con la otra (tras realizar "git merge"). Los conflictos se dan en archivos de mismo nombre con diferente contenido o en documentos que no ha conseguido integrar. La mejor manera de solucionar este error es desde la consola, abrir un editor de texto de ese archivo (en mi caso "nano <nombre-del-archivo>") y una vez abierto el editor, de manera manual ir solucionando los problemas de fusión del archivo.

3. Teniendo dos ramas (“main” y “examen_parcial”), para hacer un git merge, primero me sitúo en la rama desde la cuál quiero añadir la otra (ej. quiero integrar los cambios de "examen_parcial" en "main") primero, si estoy en examen_parcial y ya he guardado todos los cambios y hecho commit, debo salir a la rama main con **git checkout main**, una vez en main, ya sí podría hacer un merge de la otra rama con **git merge examen_parcial**. Si hubiese querido integrar "main" en "examen_parcial", debería haber hecho lo cotrario.

4. Primero haría **git log --oneline** para ver que commit deseo borrar, una vez veo su código identificador, haría **git reset <identificador_de_commit>** y así borraría el commit sin borrar los datos de guardado. (Es decir, desde ese commit daría un paso atrás al index). git reset permite deshacer cambios.

5. Para realizar un "fork", primero debo situarme en el repositorio del que deseo hacer una copia a mi cuenta de github (ya sea por un enlace facilitado o en github buscar el nombre de usuario), una vez dentro de su repositorio, arriba derecha aparece la opción fork, hago click en fork y me da la opción de clonar su repositorio a mi cuenta y así, disponer libremente de todo su contenido y poder hacer cambios. FORK se **utiliza comunmnente** para poder colaborar con otras personas en proyectos y ser capaz de editar cambios del repositorio sin que afecten al original. De esa forma, puedo probar y si hay errores no integrarlos y si consigo cambios funcionales, poder posteriormente mandarselos para que los integre a través de un **pull request** seleccionando la opción *enviar pull request desde fork*.

6. a) Primero desde la raíz, haría un ls -la (-la para ver ocultos) y así ver si existe el directorio "Nombre_del_alumno (raíz)" y así pongo **cd "Nombre_del_alumno (raíz)"**, y así sucesivamente: ls -la cd Universidad, ls -la cd UAX y finalmente ls -la para ver si existe archivo.txt.  La ruta sería **absoluta** ya que parto desde el directorio raíz.
b)  Desde Universidad, primero vería la lista de archivos que contiene **ls -la** luego cd UAX y de nuevo ls -la y finalmente vería el archivo.txt. Sería ruta relativa ya que no parto de la raíz. **Aunque si se de antemano su localización exacta, directamente con cd UAX ya me llevaría hasta el lugar que contiene el archivo.txt**

7. Opciones:
    1b) clone
    2b) git branch <nombre_rama>
    3c) git checkout
    4b) git add
    5b) git commit
    6b) git push
    7c) git pull
    8d) git merge
    9a) git reset -hard
    10c) git log

8. Proceso integración correcta:
Para integrar todos los cambios de manera limpia y satisfactoria, **primero me informaría** de los algoritmos de la rama matemáticas y los cambios de diseño UX, en este caso, es de suponer que los **cambios** de la rama UX están directamente **relacionados** con los nuevos algoritmos matemáticos. Una vez sé que tratan de lo mismo, es hora de **integrar cambios**. Como el código interno es el de la rama matemáticas y el de la vista de matemáticas es el de diseño UX, primero daría acceso a la **fusión de matemáticas** situándome en la rama develop y haciendo un rebase -i y seleccionando desde el primer commit de los nuevos algortimos. Así, a la hora de resolver problemas de fusión, irá uno a uno indicando los archivos con problemas. Una vez los tenga **integrados y sin problemas**, es hora de la **rama UX**. Sigo el mismo patrón y una vez integrados, ya habré integrado todos los cambios de ambas ramas. Ahora es momento de ver si se **visualizan corectamente**, para ello hago un open <nombre_del_archivo>. Si es correcta la visualización, la integración final en develop será **estable y funcional**.

9. c) Añadiste el botón "x^4" al archivo "index.html" en tu repositorio local, creaste un commit con los cambios y luego subiste el repositorio local al remoto en la rama principal (master).

