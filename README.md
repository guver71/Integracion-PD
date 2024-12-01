# Integracion-PD
Creación y despliegue del archivo .war en Tomcat
1. Crear el archivo .war
Sigue estos pasos para empaquetar el proyecto en un archivo .war:

Asegúrate de que tu proyecto tiene la estructura adecuada:

scss
Copiar código
/MyWebApp
  ├── WEB-INF/
  │     ├── web.xml
  │     ├── classes/  (contiene clases compiladas)
  │     └── lib/      (dependencias .jar necesarias)
  ├── META-INF/
  └── index.jsp       (u otros recursos estáticos)
Desde el directorio raíz de tu proyecto (/MyWebApp), utiliza el comando jar para empaquetar el archivo .war:

bash
Copiar código
jar -cvf MyWebApp.war *
Esto generará el archivo MyWebApp.war.

2. Subir y desplegar en Tomcat
Copia el archivo .war al directorio webapps de tu servidor Tomcat. Esto puede hacerse usando herramientas como SCP, FTP o directamente si tienes acceso al servidor:

bash
Copiar código
cp MyWebApp.war /ruta/a/tomcat/webapps/
Asegúrate de que Tomcat está ejecutándose:

bash
Copiar código
./bin/startup.sh
Tomcat desplegará automáticamente el archivo .war. Puedes verificarlo accediendo desde el navegador:

php
Copiar código
http://<IP_DEL_SERVIDOR>:<PUERTO>/MyWebApp
Por defecto, el puerto es 8080.

3. Comandos útiles
Para detener Tomcat:

bash
Copiar código
./bin/shutdown.sh
Para reiniciar Tomcat:

bash
Copiar código
./bin/startup.sh
Notas adicionales
Asegúrate de configurar correctamente el archivo web.xml en el directorio WEB-INF con los parámetros necesarios para tu aplicación.
Si necesitas personalizar el puerto o configuraciones de Tomcat, edita el archivo conf/server.xml.

Integracion en tomcat
