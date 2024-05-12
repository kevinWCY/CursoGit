CURSO DE GIT Y GIT HUB

COMANDOS DE GIT:

Que es un control de versiones?
El control de versiones es un sistema que registra los cambios realizados en un conjunto de archivos a lo largo del tiempo. Estos cambios pueden ser archivos de código fuente, documentos de texto, imágenes,
o cualquier otro tipo de archivo digital. El control de versiones permite rastrear, gestionar y coordinar el trabajo colaborativo en proyectos de desarrollo de software u otros proyectos que involucren la 
edición de archivos digitales.

Que es un repositorio?
Es el pilar de git, un repositorio es una capeta en la que se almacenan las diferentes versiones de los ficheros de un proyecto 

$ git init .- este comando se usa para iniciar un proyecto en git, te das cuenta que has hecho git init cuando se genera una carpeta .git que contiene informacion necearia para el control de versiones
esta carpeta no es visible a menos que habilites para qe te muestre los archivos ocultos

ESTADOS DE GIT
1.-modified : este es estado es cuando estas haciendo cambios en tu repo local
2.-staged : estado cuando ya lo preparas a los archicos que has modificado par que se pueda hacer un commit
3.-commited : despues de pasar por los primeros dos estados ya puedes hacer un commit 

$ git commit -m "mensaje del commit" .- se usa para guardar los cambios realizados en los archivos de un repositorio, es como guardar partida en un video juego, tienes tu puento de restauracion si te equivocas

$ git log .- te muestra el historial de los commmits que has ido haciendo en tu repositorio pero tambien te muestra los commits de los contribuyers si estas trabajando en equipo

$ git restore --staged .- Este comando saca del estado de staged a volver al estado de modified

$git push .- sirve para subir los cambios de tu repositorio local al repositorio remoto

$git clone .- sirve para clonar un repositorio remoto en tu local, es importamte que el codigo no este en privado

Que es una branch(rama) ?
Son una instancia (snapshot) de la dividion del estado del codigo
Es un nuevo apuntador hacia una de las confirmaciones

$ git branch .- este comando se usa para crear rams 

$ git switch  .- este comando se usa para cambiar de ramas 

$ git checkout -b .- tambien se usa para cambiar de rama pero esta nos direcciona directo a la rama que has creado

$ git branch -d .- se usa para eliminar lasd ramas 

FUSIONAR RAMAS

$  git marge .= trae los fusionar los cambios de la rama en donde estas y seleccinas la rama en la que quieres fusionarte

$ 
$
$
$
$
