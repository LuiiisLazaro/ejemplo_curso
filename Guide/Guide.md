![Logo Cimat](images/0cover/logoCimat.png)

#PORTADA
**Literate Programming & Continuous Integration para mejorar la calidad en la escritura de documentación técnica.**


#ÍNDICE GENERAL


#Capítulo 1 Introducción
En este capítulo se detallan las herramientas principales para realizar el taller _Creación de Libros Técnicos con Integración Continua_, impartido por el estudiante Arturo Lagunas Inocencio, como parte de su trabajo recepcional llavado a cabo durante su estancia en el Centro de Investigación en Matemáticas A.C. Unidad Zacatecas.

##Literate Programming

##Continuos Integration

##GitHub
Para el taller se trabaja con [_GitHub_](https://github.com/) herramienta utilizada para crear el repositorio donde se almacenaran los archivos correspondientes a nuestra publicación (Nuevo Libro).

##Travis-CI
[_Travis-CI_](https://travis-ci.org/) es la herramienta utilizada para llevar a cabo nuestras pruebas y realizar la integración continua, de esta manera nuestras pruebas serán realizadas de forma semiautomática, con el objetivo de encontrar fragmentos de código incorrectos y actualizarlos lo más pronto posible.

##Leanpub
[_Leanpub_](https://leanpub.com/) es la herramienta utilizada para crear nuestra publicación (libro) en la nube por decirlo de alguna manera, los cambios llevados a cabo desde nuestro repositorio serán reflejados en nuestra publicación una vez llevadas a cabo las pruebas en _Travis-CI_.

##Mejora de la Calidad en la Escritura de Documentación Técnica
Lorem

#Capítulo 2 Pasos para Crear Nuestra Publicación

En este capítulo se describen los pasos para llevar a cabo la creación de nuetra pueblicación mediante la integración de las herramientas _GitHub_, _Travis-CI_ y _Leanpub_.

##Requisitos
Pasos previos para comenzar esta guía:

* Crear Cuenta en GitHub.
    * Ingresar a [_GitHub_](https://github.com/).
    * Dar clic al botón con la opción Sign up.
    * Escribir nombre de usuario.
    * Escribir dirección de E-mail.
    * Escribir Contraseña
    * Dar clic al botón con la opción Create an account.
    * En tu correo verificar el link para confirmar la cuenta.
    * Listo! Cuenta en GitHub Creada.

* Crear Cuenta en Leanpub
    * Ingresar a [_Leanpub_](https://leanpub.com/)
    * Dar clic al boton con la opcion Sign Up.
    * Escribir tu nombre.
    * Escribir tu direccion de E-mail.
    * Modificar opcionalmente el nombre de usuario (leanpub.com/u/).
    * Escribir tu contraseña.
    * Verificar el Captcha.
    * Dar clic en Create Account.
    * Listo! Centa en Leanpub Creada.

* Crear Cuenta en Travis-CI
    * Ingresar a [_Travis-CI_](https://travis-ci.org/)
    * Dar clic al botón con la opción Sign Up.
    * Iniciar sesión con tu usuario (E-mail) y contraseña de GitHub.
    * Listo! Cuenta de GitHub vinculada en Travis-CI.

##Configuraciones Iniciales
Realizar los siguientes pasos para configurar adecuadamente nuestro entorno de trabajo.

* Crear un Nuevo repositorio:
    * Ingresar a [GitHub](https://github.com/].
    * Dar clic en el botón con la opción Sign in.
    * Iniciar sesión con tu nombre de usuario o E-mail y contraseña.
    * Dar clic en el botón con la opción Sign in.
    * Dar clic en el botón con la opción "New Repository".
    * Escribir el nombre del repositorio, en este caso "Ejemplo_curso".
    * Si lo deseas puedes agregar el archivo _README.md_, activando la casilla de verificacion: _Initialize this repository with a README_
    * Dar clic en el botón Create repository.
    * Listo! Repositorio Creado.

* Agregar el usuario Leanpub como colaborador a nuestro repositorio:
    * Dar al botón con la opción Settings.
    * Dar clic al botón con la opción Collaborators
    * Escribir el nombre de usuario Leanpub, para buscar al usuario.
    * Seleccionar el usuario leanpub Leanpub.
    * Dar clic al botón con la opción add collaborator.
    * Listo! usuario Leanpub agregado como colaborador a nuestro repositorio.

* Crar un Nuevo Libro en Leanpub:
    * Ingresar a [Leanpub](https://leanpub.com/)
    * Dar clic en el botón con la opción Sign In.
    * Iniciar sesión con tu dirección de E-mail y contraseña.
    * DAR CLIC AL BOTÓN CON LA OPCIÓN CREATE NEW BOOK
    * En la seccion New Book:
        * Escribir en nombre del libro en el campo book title.
        * En el campo Book Url, si lo deseas puedes cambiar la URL por defecto del libro.
    * En la sección How do you want to write?:
        * Seleccionar la opción Using Git and GitHub.
        * Escribir tu nombre de usuario y el nombre del repositorio para vincular en leanpub, con el orden nombreUsuario**/**repositorio. Puedes Apoyarte consultando la URL del repositorio creado con anterioridad.
        * Opcionalmente puedes activar la casilla de verificacion Send output to Dropbox para almacenar tus publicaciones en tu cuenta de Dropbox.
    * En la seccion Book Style:
        * Seleccionar la opcion Technical.
    * Dar clic en el botón con la opción Create Book.
    * Listo! Libro Creado.

* Vincular nuestro repositorio de GitHub en Travis-CI:
    * Ingresar a [Travis-CI](https://travis-ci.org/).
    * Iniciar sesión con tu cuenta de GitHub.
    * Dar clic en el botón + para agregar nuestro repositorio.
    * A continuación Travis-CI muestra una lista con nuestros repositorios almacenados en GitHub.
        * En caso de no ver una lista con nuestros repositorios, dar clic al botón con la opción Sync account.
    * Buscar el repositorio y dar clic sobre el botón con una X ubicado a la izquierda del nombre del repositorio.
    * Al dar clic, el elemento de control cambiará con una paloma en color verde.
    * Dar clic al botón en forma de engrane, para ir a las configuraciones de Travis-CI.
    * En la sección General Settings activar la opción Build only if .travis.yml is present.
    * El elemento de control cambiara a color verde de forma similar a la vinculación del repositorio.
    * Listo! Repositorio Vinculado con GitHub.

##Configuración de Archivos
Realizar los siguientes pasos para crear los archivos de configuración, los archivos son necesarios para llevar a cabo las pruebas en Travis-CI

* Crear el archivo .travis.yml
    * Ubicarnos en la raíz del repositorio creado.
    * Dar clic al botón con la opción New File.
    * Escribir el nombre del archivo: .travis.yml
    * Copiar el siguiente código del archivo [.travis.yml](https://github.com/LuiiisLazaro/ejemplo_curso/blob/master/.travis.yml)
    * Pegar el contenido en el archivo en nuestro nuevo archivo.
    *  IMPORTANTE: Modificar las líneas: 41, 50 y 51.
        * Línea 41: **- git remote add origin git@github.com:LuiiisLazaro/ejemplo_curso.git** 
            * Modificar la parte nombreUsuario/nombreRepositorio.git (**LuiiisLazaro/ejemplo_curso.git**) por tu nombre de usuario en GitHub y el nombre de tu repositorio. 
        * Línea 50: ** - git config --global user.email "luishdezlazaro@hotmail.com"** 
            * Modificar la parte de la dirección de E-mail (**"luishdezlazaro@hotmail.com"**) por tu dirección de E-mail.
        * Línea 51: **- git config --global user.name "LuiiisLazaro"** 
            * Modificar la parte nombreUsuario (**"LuiiisLazaro"**) por tu nombre de usuario en GitHub.
        * Asegurate de modificar correctamente estas líneas porque son muy importantes para realizar la publicación de nuestro libro.
    * Agregar comentario y descripcion para el commit del nuevo archivo.
    * Dar clic en el boton con la opcion Commit new file.
    * Listo! Archivo .travis.yml creado.

* Crear el archivo ez_setup.py
    * Ubicarnos en la raíz del repositorio creado.
    * Dar clic al botón con la opción New File.
    * Escribir el nombre del archivo: ez_setup.py
    * Copiar el siguiente código del archivo [ez_setup.py](https://github.com/LuiiisLazaro/ejemplo_curso/blob/master/ez_setup.py)
    * Pegar el contenido en el archivo en nuestro nuevo archivo.
    * IMPORTANTE: NO modificar ninguna linea del archivo.
    * Agregar comentario y descripcion para el commit del nuevo archivo.
    * Dar clic en el boton con la opcion Commit new file.
    * Listo! Archivo ez_setup.py creado.

* Crear el archivo script_prueba.sh
    * Ubicarnos en la raíz del repositorio creado.
    * Dar clic al botón con la opción New File.
    * Escribir el nombre del archivo: script_prueba.sh
    * Copiar el siguiente código del archivo [script_prueba.sh](https://github.com/LuiiisLazaro/ejemplo_curso/blob/master/script_prueba.sh)
    * Pegar el contenido en el archivo en nuestro nuevo archivo.
    * IMPORTANTE: NO modificar ninguna linea del archivo.
    * Agregar comentario y descripcion para el commit del nuevo archivo.
    * Dar clic en el boton con la opcion Commit new file.
    * Listo! Archivo script_prueba.py creado.

* Crear el archivo 1.Chaper1.Pnw en el directorio /manuscript/1.Chaper1.Pnw:
    * Ubicarnos en la raíz del repositorio creado.
    * Dar clic al botón con la opción New File.
    * Escribir el nombre del archivo: manuscript/script_prueba.sh
        * NOTA: el directorio manuscript se crea cuando escribes manuscript/
    * Agregar las siguientes líneas de prueba al archivo:  
        # Chapter 1  
        Hello, world!
    * Agregar comentario y descripción para el commit del nuevo archivo.
    * Dar clic en el boton con la opcion Commit new file.
    * Listo! Archivo s1.Chaper1.Pnw creado.
        * La razón del nombre 1.Chaper1.Pnw y no Chaper1.Pnw: es debido a la interpretación de Leanpub para generar nuestra publicación y mediante el prefijo # nos aseguramos de tener ordenados los capítulosen nuestra publicación.

* Generar un nuevo par de llaves SSH:
    * Desde Linux:
        * Ingresar a [Generatting a new SSH Key](https://help.github.com/articles/generating-a-new-ssh-key/).
        * Copiar el comando: ssh-keygen -t rsa -b 4096 -C "your_email@example.com" (clic derecho + copiar).
        * Abrir una Terminal.
        * Pegar el comando (clic derecho + Pegar).
        * Modificar la dirección de E-mail **your_email@example.com** por tu direccion de E-mail.
        * Presionar Enter para generar las llaves.
        * Se solicitará un nombre de archivo para guardar las llaves **(Enter a file in which to save the key (/Users/you/.ssh/id_rsa): [Press enter]**), no escribir ningún noombre solo presionar enter para continuar.
        * Se solicitará una frase de contraseña (**Enter passphrase (empty for no passphrase): [Type a passphrase]**), no escribir ninguna frase solo presionar enter para continuar.
        * Se solicitará confirmación de la frase de contraseña (**Enter same passphrase again: [Type passphrase again]**), no escribir ninguna frase solo presionar enter para continuar.
        * El par de llaves se ha generado, puedes consultarlas con el comando ls ~/.ssh/. Los nombres correspondientes son: id_rsa y id_rsa.pub.
        * Listo! llaves ssh generadas.
    * Desde Max-OS:
        * 
    * Desde Microsoft-Windows10:
        * 

* Clonar nuestro repositorio de GitHub para agregar las llaves ssh:
    * Desde Linux
        * Abrir una terminal 
        * Crear un nuevo directorio con el comando: mkdir repoLeanpub
        * Ejecutar el comando: cd repoLeanpub.
        * Ejecutar el comando: git clone https://github.com/LuiiisLazaro/ejemplo_curso
            * cambiar la URL **https://github.com/LuiiisLazaro/ejemplo_curso** por la URL de tu repositorio.
        * Ejecutar el comando: cd ejemplo_curso
            * cambiar el nombre **ejemplo_curso** por el nombre de tu repositorio.
        * Crear un nuevo directorio con el comando: mkdir .ssh 
        * Ejecutar el comando cd .ssh  
        * Copiar las llaves ssh creadas con el comando:
            * cp ~/.ssh/id_rsa .
            * cp ~/.ssh/id_rsa.pub .
            * Respetar el . al final del comando.
        * Ejecutar el comando: git status , para comprobar los cambios realizados, en este caso la creación del directorio y las llaves ssh.
        * Ejecutar el comando: git add .
        * Ejecutar el comando: git commit -am "Add ssh Keys"
        * Ejecutar el comando: git push
            * A continuación escribir el nombre de usuario o dirección de E-mail + enter.
            * Escribir la contraseña de nuestra cuenta en github + enter.
        * Listo! LLaves agregadas a nuestro directorio .ssh.
* Agregar la llave PUBLICA O PRIVADA a nuestra cuenta en GitHub.
        * Dar clic al botón con la opción View Profile and more.
        * Dar clic a la opción Settings
        * Dar clic a la opción SSH Keys.
        * Dar clic al botón con la opción Add SSH Key.
            * Escribir el titulo de LLave (nombre).
            * Abir una terminal.
            * Ejecutar el siguiente comando: cat ~/.ssh/id_rsa | id_rsa.pub
            * Seleccionar y copiar el contenido de la llave SSH
            * Pegar el contenido en el campo Key.
        * Dar clic al boton con la opcion Add Key.
        * Listo! LLave SSH agregada a nuestra cuenta.
    * Desde Mac-OS:
        * 
    * Desde Microsoft-Windows10:
        * 
    * 

* Esperar los primeros resultados en Travis-CI.
    * Verificar que las pruebas en Travis-CI han sido correctas.
    * 

* Verificación de nuestra publicación en Leanpub.
    * Ingresar a [LeanPub](https://leanpub.com/)
    * Dar clic a la opción Write.
    * Buscar nuestro libro y dar clic en el botón con la figura de engrane (settings).
    * Dar clic a la opción Preview.
    * Dar clic al botón Create Preview.
    * Esperar la creación de nuestro libro.
    * Verificar el contenido con cualquiera de los archivos generados (.pdf, .epub o .mobi)

* Realizar el tutorial para aprender la sintaxis de Markdown
    * Ingresar a [markdowntutorial](http://markdowntutorial.com/)
    * Realizar las lecciones