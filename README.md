# Manual
1. Abre linux
2. Abre el terminal
3. entra en el Github del profe "rusben"
4. entra donde pone "Instal·lacions i configuracio de clouds"
5. Entras en el manual de isntalacion de aplicaciones webs
6. Primero tiene que poner el codigo que esta hay te pedira un acontraseña que es "usuario"
7. Despues haz el segundo paso que te actualiza la maquina
8. Cuando se descargue haz el siguente codgo "sudo apt install -y apache2" eso comando te descarga el servidor web apache2
9. Despues tiene que poner el siguiente codigo "sudo apt insall -y mysql-server" y lo que hace es descargar el servidor de base de datos
10. Al terminar tendras que poner el los dos siguientes comandos "sudo apt install -y php libapache2-mod-php" y "sudo apt install -y php-fpm php-common php-mbstring php-xmlrpc php-soap php-gd php-xml php-intl php-mysql php-cli php-ldap php-zip php-curl" que lo que hacen es insatalr algunas librerias de php que es el lnguage principal que se utilizan las aplicaciones
11. al terminar las instalaciones  hay que reiniciar el servidor de apache2 con este comando "sudo systemctl restart apache2"
12. Ahora pasaremos a la configuracion del MySQL
13. Des del terminal donde seamos root tenemos que ejecutar el siguente comando "sudo mysql"
14. Ahora crearemos la base de datos
15. Dospues de tener la consola de MySQL ejecutamos los comandos para crear la base de datos en etse caso estamos creando una base de datso qcon el nombre "ddbb" pero puedes ponerle cual quier nombre
16. Ahora despues de crear la base de datos craremos un usuario
17. Hay que tener en cuanta que se tendra que identificar la ip des de donde se accedera a la base de datos en este caos es localhost este es el comando que tendars que poner para crear el usuario "CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';  
