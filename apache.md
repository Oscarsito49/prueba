# Apache

## Introducción:
### Resumen


### Palabras clave:
1. 
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



### Motivación:



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



#### Paso 2: Ajustar el Firewall
Antes de probar Apache, es necesario modificar los ajustes de firewall para permitir el acceso externo a los puertos web predeterminados. Suponiendo que siguió las instrucciones de los requisitos previos, debería tener un firewall UFW configurado para que restrinja el acceso a su servidor.

Durante la instalación, Apache se registra con UFW para proporcionar algunos perfiles de aplicación que pueden utilizarse para habilitar o deshabilitar el acceso a Apache a través del firewall.

Enumere los perfiles de aplicación ufw escribiendo lo siguiente:
![7](https://github.com/user-attachments/assets/e53b9325-20f7-4906-a67f-9c4baa7e9605)




### Configuración












## Bibliografía
### Classsroom: 
**GitHub Introducció _de Daniel Delgado_**

### Externos:

[Instalación](https://www.digitalocean.com/community/tutorials/how-to-install-the-apache-web-server-on-ubuntu-20-04-es?authuser=0)  
[Configuración](https://ubuntu.com/tutorials/install-and-configure-apache#1-overview)  
[Virtual Host](https://www.desarrollolibre.net/blog/apache/que-son-y-como-emplear-los-virtualhost-en-apache)  
