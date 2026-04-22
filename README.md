# Trabajo individual
Jherson Godoy Montaño

# Clase 1
### ¿Que es GIT?
Es un sistema de control de versiones distribuido, Este nos permite guardar archivos y las versiones de estos a lo largo del tiempo de manera local
![imagen de git](img/git.png)
### ¿Como nacio GIT?
GIT nacio un en abril del 2005 creado por Linus Torvalds, antes de siquiera pensar en la creacion de git exitia lo que es Bitkeeper y el señor Torvals usaba este ya que era gratuito peroun dia los de Bitkeeper decidieronempesar a cobra por los usos de este cosa que no le gusto a linus Torval por lo que enojado decidio encerarse en su cuarto unas 2 a 3 semana para crear algo mejor  que Bitkeeper y asi nacio por un enfado xd
![Creador de GIT](img/creador.png)
### ¿Como instalar GIT?
#### En windows
Simplemente tienes que :
  * ir a tu buscador favorito
  * buscar git y apretar en downloads
  * aceptar las configuraciones segun tu gusto
  * verificar la instalacion con git --version en el cmd
#### En linux
 Casi lo mismo que windoons pero:
  * vas a tu navegador
  * buscas git y entras en la parte que dice linux
  * copias el codigo segun la distrubucion que tengas
  * lo pegas en tu terminal 
  * revisas que se instalo con git --version en la terminal
![Sistemas operativos](img/OP.png)
### Configuraciones Básicas 
 * git config --global user.name "Tu Nombre"
 * git config --global user.email "tu@correo.com"
 * git config --global core.autocrlf true
# Clase 2
### States y commits
* **STATES** sirve para inicialisar el guardado y cuales quieres guardar
* **COMMITS** es el comentario que subes para decir que cambio hiciste
![imagen chistosa](img/imagenchistosa.png)
### Los estados de GIT
#### Directorio de trabajo(Modificado)
Este una carpeta en la que GIT observa tus archivos y los cataloga en:
* **Untracked** Es decir sin seguimiento osea ve el archivo pero no tiene unseguimiento ni versiones antiguas de este. 
* **Modified** Es con una version antigua guardada un archivo que guardaste y que quieres modificar

#### ¿Que pasa si el archivo no me gusto y quiero que se quede la version anterior?
Para pasar de Modified a suestado original solo tienes que hacer este codigo
* **git restore <archivo>**
esto borra todo lo que se escrivio en la ultima entrada

#### ¿Que pasa si quiero que un archivo no se vea?
Para quetu codigo funcione pero no se vea tus patrones o tokens o algo que no quieres que sea publico se crea la carpeta **gitignore**  en este entrara todo tus datos 
#### Stage area(Preparado)
seleciona archivos modificados que se incluiran en el sigiuente commit (guardado)
* **git add<archivo>** Agrega un archivo solo el que eliges 
* **git add .:** Agrega todos los archivos que este observados por git
si quieres sacar un archivo del stage area para volver al anterior 
** git restore --staged <archivo>**
#### Repositorio local
Aqui es cuando ya estamos decididos a subir el proyecto y guardar los cambios para quepasen a ser parte del historial
* **git commit -m "mensaje"**
y si quieres desaserte de tu ultimo commmit solo tienes que hacer:
* **git reset --soft HEAD~1**

![estados de git](img/estados.png)


### Buenas practicas 
#### ¿Cada cuanto hacer un commit?
Usar los commits atómicos. son una práctica de git donde cada confirmacion(commit)representa un cambio logico pequeño o que no afecte tanto 
### ¿Escribe buenos commits?
un commmit debe de ser muy corto y muy descriptivo por eso se usa :
**1 Verbos imperativos(Add,change,fix,remove)**
*  **Add** Significa que se añade un archivo
* **Change** Significa que se modifica unarchivo existente
* **Fix** Significa que se arreglo un BUG
* **Remove** significa que se elimina un archivo existente
**2 NO uses punto final ni suspensivos**
usar puntuacion mas allá de las comas es innecesarioa la hora de crear un buen mensaje

**3 no usar mas de 50 caracteres**
se corto y conciso si no tienes mucho que explicar es probable que tu commit contenga demaciado cambias
**4 usar un prefijo para hacerlos mas semanticos**
para que tu historial sea mas legible
* **git commit -m "<tipo de commit>: <Descripcion>"**
* **git commit -m "feat:add new search feacture"**

**Escribe buenos commits**
* **feat:** para una nueva característica para el usuario.
* **fix:** para un bug que afecta al usuario.
* **perf:** para cambios que mejoran el rendimiento del sitio.
* **build:** para cambios en el sistema de build, tareas de despliegue o instalación.
* **ci:** para cambios en la integración continua.
* **docs:** para cambios en la documentación.
* **refactor:** para refactorización del código como cambios de nombre de variables o funciones.
* **style:** para cambios de formato, tabulaciones, espacios o puntos y coma, etc; no afectan al usuario.
* **test:** para tests o refactorización de uno ya existente

**5 añadir contexto al cuerpo del commit**
En ves de saturar el sumario de commit añade informacion nesesaria en el cuerpo del mensajeen aqui si puedes usar reglas de puntuacion
*git commit*
*prefijo:Titulo de tu commit*
*cuerpo que describe tu commit*
