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

ESTADOS DE GIT:

1.-modified : este es estado es cuando estas haciendo cambios en tu repo local
2.-staged : estado cuando ya lo preparas a los archicos que has modificado par que se pueda hacer un commit
3.-commited : despues de pasar por los primeros dos estados ya puedes hacer un commit 

$ git commit -m "mensaje del commit" .- se usa para guardar los cambios realizados en los archivos de un repositorio, es como guardar partida en un video juego, tienes tu puento de restauracion si te equivocas

$ git commit -am -m .- este comando se usa para sobreescribir en el commit que hiciste recientemente ,se usa para cuando cometes un error en el commit

$ git log .- te muestra el historial de los commmits que has ido haciendo en tu repositorio pero tambien te muestra los commits de los contribuyers si estas trabajando en equipo

$ git restore --staged .- Este comando saca del estado de staged a volver al estado de modified

$ git push .- sirve para subir los cambios de tu repositorio local al repositorio remoto

$ git clone .- sirve para clonar un repositorio remoto en tu local, es importamte que el codigo no este en privado

$ git remote -v .- se usa para ver al repositorio remoto al que estas enlasado 

$ git push origin <rama> .- se usa para subir los cambios a una rama especifica 

$ git push --all .- se usa para subir todas las ramas que tienes en tu repo local a tu remoto de una sola vez 

$ git branch -a .- este comando se usa para ver las ramas invisibles por asi decirlo, esto pasa cuando haces un git pull y las ramas qwe crearon tus companieros no se pueden visualizar 

$ git fetch .- se usa para actualizar lo que hay en el repositorio remoto actual en tu repositorio local 

$ git pull .- se usa para recuperar cambios de la rama remota al que estas enlazada 

$ git pull <rama1> <rama2> <rama n> .- este comando especifica las ramas de la que quieres traerte los cambios

QUE ES UNA RAMA?
Son una instancia (snapshot) de la dividion del estado del codigo
Es un nuevo apuntador hacia una de las confirmaciones

$ git branch .- este comando se usa para crear rams 

$ git switch  .- este comando se usa para cambiar de ramas 

$ git checkout -b .- tambien se usa para cambiar de rama pero esta nos direcciona directo a la rama que has creado

$ git branch -d .- se usa para eliminar ramas 

FUSIONAR RAMAS:

$  git merge .= se usa para fusionar las ramas, por ejemplo si tu te creas un nueva rama y tienes otra rama donde ya has tienes codigo avanzado, si haces merge de esa rama que ya tenias 
a tu rama nueva tendras todo ese codigo avanzado en tu rama nueva

CONFLICTOS EN GIT
GIT HUB:

Sincronizar repositorio local con el repositorio remoto

$ git remote add origin https://... .- se utiliza para agregar un nuevo origen remoto a un repositorio Git local.

$ git push origin main .- se usa para subir los cambios de tu repositorio local a tu repositorio remoto

clonar un repositorio:

$ git clone https://... .- se usa para colaborar en un repositorio que no te pertenece

MALAS PRACTICAS DE COMANDOS:

$ git push -f origin main .- se usa para subir cambios pero en este caso con el -f estan forzando subir los cambios por lo que nos generaria conflictos 

QUE ES PULL REQUEST?

Los pull requests son una forma efectiva de colaborar en proyectos de código abierto y en equipos de desarrollo, ya que proporcionan un mecanismo transparente para revisar, discutir y aprobar cambios antes de que se incorporen al proyecto principal.

FLUJOS DE TRABAJO:

Los flujos de trabajo en el contexto de desarrollo de software se refieren a los procesos y las prácticas que un equipo o una organización sigue para llevar a cabo el desarrollo, la revisión, la prueba y la implementación de software. Estos flujos de trabajo establecen una serie de pasos y reglas que guían cómo se realizan estas actividades en el día a día del desarrollo de software.

Tipos de flujo de trabajo:

Git Flow(antiguo).- Este es un modelo de flujo de trabajo popular basado en Git que define una serie de ramas específicas y reglas para su uso. Incluye ramas como master, develop, feature, release, y hotfix, y se centra en la estabilidad del código y la gestión de versiones.

GitHub Flow.- Este flujo de trabajo simplificado se centra en una sola rama principal (generalmente main o master) y utiliza pull requests para gestionar los cambios en el código. Es especialmente adecuado para proyectos con ciclos de desarrollo rápidos y continuos despliegues.

Trunk Based Development.- En este enfoque, todos los cambios se realizan directamente en la rama principal del repositorio (trunk). Se basa en la filosofía de integración continua y se centra en mantener un código estable y siempre desplegable.

Ship/Show/Ask.-
Ship (Enviar): En este paso, el desarrollador finaliza y envía los cambios al repositorio principal del proyecto. Esto implica completar el trabajo en la funcionalidad o los cambios, realizar pruebas necesarias y asegurarse de que el código esté listo para ser fusionado en el repositorio principal.

Show (Mostrar): Después de enviar los cambios, el desarrollador muestra o comunica la nueva funcionalidad o los cambios al equipo de desarrollo o a otras partes interesadas. Esto puede incluir realizar demostraciones, compartir capturas de pantalla o presentar la funcionalidad en un entorno de prueba.

Ask (Preguntar): En este paso, el desarrollador solicita retroalimentación sobre los cambios enviados y mostrados. Puede preguntar al equipo sobre aspectos específicos de la implementación, solicitar revisiones de código o comentarios sobre la usabilidad y la funcionalidad. El objetivo es recopilar comentarios y mejorar los cambios antes de que se integren por completo en el proyecto.

DESHACER CAMBIOS:

Se aplica cuando hay un error grave en el proyecto 

En que casos deshacemos los cambios?
- deja de funcionar el proyecto
- queremos recupera una parte del codigo que eliminamos
- queremos recuperar archivos que eliminamos

COMANDOS DESTRUCTIVOS Y NO DESTRUCTIVOS:

$ git reset --hard <hash commit> .- me elimina todos los commits arriba del hash commit qe seleccionas, tambien me elimina las modificaciones de codigo
$ git reset --soft <hash commit> .- me elimina todos los commits arriba del hash commit qe seleccionas, en este caso me conserva las modificaciones hechas
$ git reset --soft HEAD ~n
$ git reset --abort 
$ git restore 
$ git revert .- staged vuelve a modified
$ git revert <hash commit>.- genera conflictos al hacer git revert


