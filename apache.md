# Apache

## Introducción:
### Resumen


### Palabras clave:
1. **APACHE**
2. 
3. 
4. 
5. 
6. 
7. 
   
### Índice:
[-Introducción](#Introducción)    
[-Palabras Clave](#Palabras-clave)    
[-Contexto](#Contexto)    
[-Motivación](#Motivación)    
[-Instlación](#Instalación)    
[-Configuración](#Configuración)    
[-Bibliografia](#Bibliografía)    


### Contexto:
Este proyecto se lleva a cabo en un entorno académico, en el que los estudiantes aprenden sobre tecnologías de servidores web, en particular Apache. El objetivo de esta actividad es brindar una comprensión básica de los servidores web, su configuración y funcionamiento, así como su rol en la arquitectura de la web.

Apache es uno de los servidores web más utilizados a nivel mundial. Fue desarrollado por la Apache Software Foundation y lanzado en 1995. Es un servidor web de código abierto y gratuito que permite alojar sitios web y aplicaciones. Su flexibilidad y compatibilidad con diferentes sistemas operativos (como Unix, Linux y Windows) lo han convertido en una opción popular para desarrolladores y empresas.

Apache permite gestionar solicitudes HTTP y servir contenido web estático o dinámico. Se utiliza tanto en entornos de producción como de desarrollo, y su arquitectura modular permite añadir funcionalidades adicionales a través de módulos que amplían sus capacidades.

Posibles alternativas a Apache:
* Nginx: Un servidor web y proxy inverso, conocido por su rendimiento en entornos de alta concurrencia. Es ligero y adecuado para sitios de alto tráfico.
* Microsoft IIS: Servidor web de Microsoft, optimizado para funcionar con productos de Microsoft y el sistema operativo Windows, y con una integración excelente con .NET.
* LiteSpeed: Otro servidor web de alto rendimiento, especialmente adecuado para sitios que necesitan optimización de velocidad y soporte en tecnologías específicas como WordPress.


### Motivación:
El motivo principal de este proyecto es comprender el funcionamiento de Apache como servidor web y su rol esencial en la gestión de sitios y aplicaciones web. A través de esta experiencia, buscamos adquirir habilidades prácticas en la configuración y administración de servidores, entendiendo cómo Apache permite alojar y servir contenido de forma eficiente. Esta práctica nos ayudará a construir una base sólida en tecnologías de servidores web, facilitando nuestra preparación para futuros proyectos y entornos profesionales.


## Cuerpo:
### Instalación
#### Paso 1: Instalar Apache
Apache está disponible en los repositorios de software predeterminados de Ubuntu, lo que permite instalarlo con las herramientas convencionales de administración de paquetes.

Comencemos actualizando el índice de paquetes locales para que reflejen los últimos cambios anteriores:
![1 (1)](https://github.com/user-attachments/assets/e9d8715c-ee52-440d-a876-fdefb35148c0)  
A continuación, instale el paquete **apache2**:  
![2](https://github.com/user-attachments/assets/0c8786a8-6b1f-4b21-9d8c-015f00a91494)

En este caso nos sale un error por lo que procedemos a killear un proceso que nos impide la instalacion y volver a intentarlo:
Matar el proceso:  
![3](https://github.com/user-attachments/assets/15e7c5fe-d1f6-489c-948d-b16303563cf7)

Volver a instalarlo:  
![4 (2)](https://github.com/user-attachments/assets/2596bed3-1829-418c-a5bd-29d868732b12)
![5](https://github.com/user-attachments/assets/15fdaa56-b838-4edd-806e-a6ab448b2f41)
![6](https://github.com/user-attachments/assets/962b4228-8af2-45ca-b237-09efc5daf66e)  

En este caso ya nos dejo realizar la instalación.


#### Paso 2: Ajustar el Firewall
Antes de probar Apache, es necesario modificar los ajustes de firewall para permitir el acceso externo a los puertos web predeterminados. Suponiendo que siguió las instrucciones de los requisitos previos, debería tener un firewall UFW configurado para que restrinja el acceso a su servidor.

Durante la instalación, Apache se registra con UFW para proporcionar algunos perfiles de aplicación que pueden utilizarse para habilitar o deshabilitar el acceso a Apache a través del firewall.

Enumere los perfiles de aplicación ufw escribiendo lo siguiente:  
![7](https://github.com/user-attachments/assets/e53b9325-20f7-4906-a67f-9c4baa7e9605)   
![8](https://github.com/user-attachments/assets/a8a9efc9-bd20-4e10-868a-ede77c239dbb)  
Puede verificar el cambio escribiendo lo siguiente:  
![9](https://github.com/user-attachments/assets/a6b84dc7-e8c8-4f50-9f07-32e12ab0e517)


#### Paso 3: Comprobar su servidor web
Al final del proceso de instalación, Ubuntu 20.04 inicia Apache. El servidor web ya debería estar activo.

Realice una verificación con el sistema init systemd para saber si se encuentra en ejecución el servicio escribiendo lo siguiente:  
![10](https://github.com/user-attachments/assets/e01da906-54aa-4b52-ad45-7de4d6eb0da5)  
Como lo confirma este resultado, el servicio se inició correctamente. Sin embargo, la mejor forma de comprobarlo es solicitar una página de Apache.

Puede acceder a la página de destino predeterminada de Apache para confirmar que el software funcione correctamente mediante su dirección IP: Si no conoce la dirección IP de su servidor, puede obtenerla de varias formas desde la línea de comandos.

Intente escribir esto en la línea de comandos de su servidor:  
![11](https://github.com/user-attachments/assets/84e29b74-4394-4daa-916c-ced5f4e2aa8e)  
Cuando tenga la dirección IP de su servidor, introdúzcala en la barra de direcciones de su navegador:  
Debería ver la página web predeterminada de Apache en Ubuntu 20.04:  
![12](https://github.com/user-attachments/assets/a49cf47f-d622-4cdf-928b-8afe03a6e7c3)  
Esta página indica que Apache funciona correctamente. También incluye información básica sobre archivos y ubicaciones de directorios importantes de Apache.


### Configuración
#### Creando nuestro propio sitio web
Por defecto, Apache viene con un sitio básico (el que vimos en el paso anterior) habilitado. Podemos modificar su contenido en /var/www/htmlo en su configuración editando su archivo Virtual Host que se encuentra en /etc/apache2/sites-enabled/000-default.conf.

Podemos modificar la forma en que Apache maneja las solicitudes entrantes y tener múltiples sitios ejecutándose en el mismo servidor editando su archivo Virtual Hosts.

Hoy, dejaremos la configuración de host virtual Apache predeterminada apuntando a www.example.com y configuraremos la nuestra en gci.example.com.

Entonces, comencemos creando una carpeta para nuestro nuevo sitio web /var/www/ejecutando  
![21](https://github.com/user-attachments/assets/e265d9db-cc96-4168-a4c4-819d040a8f17)  
Lo hemos nombrado gci, pero cualquier nombre funcionará, siempre que lo indiquemos en el archivo de configuración de hosts virtuales más adelante.

Ahora que hemos creado un directorio para nuestro sitio, vamos a colocar un archivo HTML en él. Vayamos al directorio que acabamos de crear y creemos uno escribiendo:  
![22](https://github.com/user-attachments/assets/b2dff40e-67d3-453b-8952-11c4c79e6afb)  
Pegue el siguiente código en el index.html archivo:  
![23](https://github.com/user-attachments/assets/de3a21a2-9979-4f2f-9d23-2507c9d309b1)  
Bastante genial, ¿verdad?

Ahora vamos a crear un archivo VirtualHost para que aparezca cuando escribamos gci.example.com.

#### Configuración del archivo de configuración de VirtualHost
Comenzamos este paso yendo al directorio de archivos de configuración:
`cd /etc/apache2/sites-available/`

Dado que Apache viene con un archivo VirtualHost predeterminado, usémoslo como base. ( gci.confse usa aquí para que coincida con nuestro nombre de subdominio):
`sudo cp 000-default.conf gci.conf`

Ahora edite el archivo de configuración:
`sudo nano gci.conf`
![24](https://github.com/user-attachments/assets/f7fb907e-7e24-4437-9a65-0b0d8cc71cb5)  

Deberíamos tener nuestro correo electrónico para ServerAdminque los usuarios puedan comunicarse con usted en caso de que Apache experimente algún error:
`ServerAdmin yourname@example.com`

También queremos que la DocumentRootdirectiva apunte al directorio en el que están alojados los archivos de nuestro sitio:
`DocumentRoot /var/www/gci/`

El archivo predeterminado no viene con una ServerNamedirectiva, por lo que tendremos que agregarlo y definirlo agregando esta línea debajo de la última directiva:
`ServerName gci.example.com`
![25](https://github.com/user-attachments/assets/55bdd463-296a-433c-be41-98a7f2e01517)

#### Activación del archivo VirtualHost
Después de configurar nuestro sitio web, debemos activar el archivo de configuración de hosts virtuales para habilitarlo. Para ello, ejecutamos el siguiente comando en el directorio del archivo de configuración:
`sudo a2ensite gci.conf`

Deberías ver el siguiente resultado
`Enabling site gci.`

```
To activate the new configuration, you need to run:
  service apache2 reload
root@ubuntu-server:/etc/apache2/sites-available#
```

Para cargar el nuevo sitio, reiniciamos Apache escribiendo:
`service apache2 reload`
![26](https://github.com/user-attachments/assets/6c811214-7508-4d98-9f9b-dc918b6b4ec9)  
Deberemos poner la contraseña de nuestro ususario en caso de tener una:  
![27](https://github.com/user-attachments/assets/46126cf9-999a-4af4-8fc1-d39322f38962)

Resultado final:  
![28](https://github.com/user-attachments/assets/a22d2caa-8bdf-4c88-9c31-50ec3847be05)






## Resultados y Conculsión







## Bibliografía
### Classsroom: 
**Documentación de APACHE Introducción _de Daniel Delgado_**
**Documentación de APACHE Configuración _de Daniel Delgado_**

### Externos:

[Instalación](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04-es?authuser=0)  
[Configuración](https://ubuntu.com/tutorials/install-and-configure-apache#1-overview)  
[Virtual Host](https://www.desarrollolibre.net/blog/apache/que-son-y-como-emplear-los-virtualhost-en-apache)  
