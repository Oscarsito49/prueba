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





## Resultados y Conculsión







## Bibliografía
### Classsroom: 
**Documentación de APACHE Introducción _de Daniel Delgado_**
**Documentación de APACHE Configuración _de Daniel Delgado_**

### Externos:

[Instalación](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04-es?authuser=0)  
[Configuración](https://ubuntu.com/tutorials/install-and-configure-apache#1-overview)  
[Virtual Host](https://www.desarrollolibre.net/blog/apache/que-son-y-como-emplear-los-virtualhost-en-apache)  
