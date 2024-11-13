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
17. Hay que tener en cuanta que se tendra que identificar la ip des de donde se accedera a la base de datos en este caos es localhost este es el comando que tendars que poner para crear el usuario "CREATE USER 'usuario'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';"
18. Ahora hay que darle pribilegios al usuario con este comando "GRANT ALL ON bbdd.* to 'usuario'@'localhost';"
19. Al terminar tienes que salir de la base de datos poniendo exit
20. Ahora tiens que descargar el zip de ownCloud Server
21. Despues de tenerlo descargado entra en donde la tienes ubicada y cambiale el nobre a app-web.zip
22. Ahora coloca el siguente comando pero tiene que canbiar una cosa donde pone Baixades si lo tienes en otro dioma que no sea el catalan tienes quue poner Descarga este es el comando "sudo cp ~/Baixades/app-web.zip /var/www/html"
23. Ahora hay que ir al directorio con este comando "cd /var/www/html"
24. Ahora tiens que decomprimir el fixero que emos descargado con este comando "sudo unzip app-web.zip"
25. Despues hay que copiar los fixeros en la carpeta /var/www/html canvia el nombre app-web por el nombre de directorio donde se halla decomprimido vustro archivo "sudo unzip app-web.zip"
26. Al terminar elimina la carpeta creada con este comando "sudo unzip app-web.zip"
27. Ahora tiens que eliminar el fixero index.html del apache2 con este comando "sudo rm -rf /var/www/html/index.html"
28. Ahora hay que descargar los requisitos previos de PPA con este comando "sudo apt install software-properties-common -y"
29. Cuando lo tengas tiens que instalar las herramientas nesesarias para trabajar connel arxivo de paquetes peronales(PPA) con este codigo "LC_ALL=C.UTF-8 sudo add-apt-repository ppa:ondrej/php -y"
30. Ahora acutaliza los repositorios con este comando "sudo apt update"
31. Cuando lo actualizes tieens que insatlar las librerias de PHP de la version 7.4 Son los siguentes codigos "sudo apt install php7.4 -y", "sudo apt install -y php libapache2-mod-php7.4" y "sudo apt install -y php7.4-fpm php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-gd php7.4-xml php7.4-intl php7.4-mysql php7.4-cli php7.4-ldap php7.4-zip php7.4-curl"
32. Ahora tieneq ue selecionar la version de PHP que quieras con este comando "sudo update-alternatives --config php"
33. Cuando hallas selecionado la vercion tienes que activar los modulos de apache2 nesesarios con estos dos comandos "sudo a2enmod proxy_fcgi setenvif" y "sudo a2enconf php7.4-fpm"
34. Por ultimo reinisia la apache2 con este ultimo comando "sudo service apache2 restart" 
