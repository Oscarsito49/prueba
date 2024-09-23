# GitHub + Markdown by Oscar Blei

## Introducción:

### Que es GitHub
**GitHub** es una plataforma en línea que permite a los desarrolladores **colaborar y gestionar** proyectos de software utilizando **Git**, un sistema de control de versiones distribuido. **GitHub** proporciona herramientas para que los programadores puedan trabajar juntos en el mismo código, hacer seguimiento de cambios, y gestionar versiones de un proyecto.

### Usos principales de GitHub:
1. **Control de versiones:** Permite a los equipos de desarrollo llevar un registro de todos los cambios realizados en un proyecto, facilitando la reversión de errores o la comparación entre versiones del código.
2. **Colaboración:** Los equipos pueden colaborar fácilmente, incluso si están distribuidos geográficamente. Pueden crear “pull requests” para proponer cambios que luego se revisan antes de incorporarlos al proyecto principal.
3. **Repositorios de código:** Un repositorio (o “repo”) es donde se almacena todo el código de un proyecto. GitHub permite que los repositorios sean públicos o privados.
4. **Gestión de proyectos:** Ofrece herramientas de organización como issues (problemas o tareas), proyectos Kanban, y milestones para planificar y gestionar el desarrollo de software.
5. **Automatización y CI/CD:** GitHub Actions es una funcionalidad que permite automatizar procesos como pruebas, compilación, y despliegue de aplicaciones.
6. **Documentación:** Además del código, los repositorios en GitHub permiten agregar documentación (por ejemplo, usando archivos README o wikis) para explicar el propósito y el uso de los proyectos.
7. **Contribución de código abierto:** Gran parte de los proyectos de código abierto están alojados en GitHub, lo que facilita a los desarrolladores contribuir a proyectos en todo el mundo.
   
### Finalidad de MI documento:
En **este documento** mostrare diferentes funciones de **GitHub**, así como los passos a seguir y aquella informacion que considere importante.

## Pasos a seguir para conseguir diferenres acciones.
### Intsalar GitHub en Mac/Osx

La forma **más fácil** de instalar **Git en Mac** es a través del instalador que puede descargar [aquí](https://sourceforge.net/projects/git-osx-installer/files/). Abre el archivo que acabas de descargar y sigue las instrucciones para realizar la instalación.

Para **confirmar** que la instalación de GIT **es correcta**, abre una nueva ventana de Terminal y escribe el siguiente comando:
```
git --version
```
Si **GIT** está instalado, el comando de arriba debería mostrar la versión instalada actual.

## Crear archivo
A continuación vamos a crear un archivo en c que usaremos para aprender los comandos básicos de **GitHub**,
```
$ mkdir pruebaGitHub
$ cd pruebaGitHub
$ touch prueba.c
$ gedit % nano ~/Documents/readme.txt
```
En este momento se debe de abrir un editor de textos para poder escribir el contenido del programa:
```
#include <stdio.h>
int main(){
    printf(“Hola DAW”);
    return 0;
}
```

## Configurar GIT y subir archivos
Antes de continuar usando GIT, debes configurar tu nombre de usuario y correo electrónico. Estos detalles se asociarán con cualquier confirmación que crees. Para configurarlo, ejecuta los siguientes comandos:
```
$ git config --global user.email “<miCorreoElectrónicoEnGitHub>”
$ git config --global user.name “<miNombreEnGitHub>”
```
A continuación procedemos a iniciar un nuevo repositorio en GitHub y subir el directorio actual:
```
$ git init
$ git add .
$ git commit -m “Subida del archivo de prueba”
$ git push
```
Es posible que en algún momento pida un token de GitHub. Se pueden obtener en **GitHub → Settings** de la cuenta **→ Developer Settings** (A la izquierda, abajo del todo) **→ Personal access tokens → Generate new token.**

**Comprueba en la web de Github que tu archivo se ha subido correctamente.**



## Conclusiones
**GitHub** es una herramienta fácil de usar que simplifica el proceso de programación, permitiendo a los desarrolladores subir archivos y gestionar proyectos de manera centralizada en la nube. Con una interfaz intuitiva y basada en Git, puedes controlar versiones de tu código, colaborar con otros programadores de forma sencilla y mantener todo organizado en un solo lugar. Además, al estar todo en la nube, puedes acceder a tus proyectos desde cualquier lugar, lo que facilita la gestión, el trabajo colaborativo y la integración continua en tus flujos de desarrollo.

## Bibliografía
### Classsroom: 
**GitHub Introducció _de Daniel Delgado_**
