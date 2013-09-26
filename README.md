Bievenido este va a hacer el repositorio
para el proyecto: __

======

Esto es para las pruebas de primera instancia de aprendizaje
------------

El primer paso es registrarse en http://github.com , muy importante recordar tus datos de correo y direccion, los usarás al configurar el cliente en linux.

Paso 2 : Dejamos un momento de lado la web de github y abrimos una terminal, ahí vas a buscar/instalar los siguientes paquetes: git-core, git-gui, y git-doc. Particularmente nunca he encontrado git-doc en Fedora, pero no hay problema, los que nos interesan son git-gui y git-core.


Paso 3: Una vez instalados en la misma terminal vamos a configurar las llaves SSH, lo primero es checar si ya existe una carpeta llamada .ssh en tu home. Esto lo haces simplemente dirigiendote desde la terminal a dicha carpeta..

cd ~/.ssh

Si te dice que no existe la carpeta salta al paso 5 ,sino ve al paso siguiente..

Paso 4: Si la carpeta .ssh existe, hay que hacer un respaldo introduciendo lo siguiente:

mkdir key_backup
cp id_rsa* key_backup
rm id_rsa*

Lo cual creara una carpeta de respaldo de las llaves actuales y las movera a dicha carpeta.

Paso 5: Se necesita generar una nueva llave SSH, para esto introduce:

ssh-keygen -t rsa -C "tu@correo.com"

Introduciendo tu correo entre comillas..

Despues te preguntara en donde deseas guardar la llave, no escribas nada y presiona enter, de esta forma se creara la carpeta .ssh con tus llaves.

Y luego te pedira una contraseña, ésta será requerida cada que hagas un movimiento en github, lo recomendable es siempre establecer una, aunque tambien puede quedar en blanco (presionando enter).

Al final verás una imagen (huella digital) en ascii lo cual significa que ya está listo.

Paso 6:  Ve a tu carpeta .ssh y busca el archivo  id_rsa.pub, selecciona y copia todo el texto que está ahí.

Ahora en Github ve a Account>SSH Public keys. Si ya has creado una llave y como yo estas volviendo a configurarla, hay que editar la que esta actualmente, de lo contrario da clic Add another public key, Introduce el nombre de tu llave (puede ser cualquiera) y abajo la clave que copiaste anteriormente. Guarda los cambios.

Paso 7:  De nuevo en la terminal es hora de probar que todo funcione, introduce:

ssh -T git@github.com

Te dira que no se puede establecer la autenticidad del host y que si deseas continuar (a palabras resumidas) le decimos yes y enter

Paso 8: Ahora toca introducir nuestros datos los cuales apareceran cada que hagamos algun movimiento a nuestro repositorio.

Para empezar vamos a establecer nuestro nombre introduciendo en la terminal :

git config --global user.name "Nombre Apellido"

De forma seguida, vamos a introducir nuestro correo:

git config --global user.email "tucorreo@mail.com"
--------------------------------------------------------------------------------------------------------------------------------------------------------------------
-get init(crear repositorio).}
-touch README2 //crear archivo de lectura.
-git add README2(añadir archivo al repositorio).
-git status.(ver estatus del repositorio).
-git commit -m "este es el primer archivo desde server_teo" cambio al repositorio local
- git remote add origin (https://github.com/mateovelilla/prueba.git) esta direccion es de la pagina del repositorio al que se desea conectar para realizar los commit.
-git pull origin master (aqui se trae el repositorio en este momento).
-git push origin master(se sube el archivo que se tiene en el repositorio).





