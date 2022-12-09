ASTERIX DECODER

En esta carpeta se adjunta lo siguiente:
-El codigo utilizado del programa
-La memoria donde se muestro como se ha realizado el código
-Los ficheros pertinentes para llevar a cabo las simulaciones con el decodificador.

El lenguaje utilizado es C# en Visual Studio (la última versión). A parte se ha utilizado la extensión GMAP.NET para el mapa.

--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

Este decodificador lee datos de CAT10 y CAT21 v2.1 . Hay diferentes clases para ello:

*ClassLibrary:   
    -AsterixFile: desde esta clase leemos los ficheros .ast con los cuales trabajaremos. Por otro lado, se crean las listas y tablas donde se almacenará la infomación correspondiente a los archivos asterix. Desde aquí se llama a las clases CAT10 y CAT21, en función del tipo de mensaje que sea para que se calculen los data items del paquete en cuestión.

    -CAT10: esta clase contiene el codigo necesario para decodificar un mensaje de categoria 10. Esta clase es llamada desde AsterixFile.

    -CAT21: esta clase contiene el codigo necesario para decodificar un mensaje de categoria 21. Esta clase es llamada desde AsterixFile.

    -Flight: esta clase se usa para poder representar gráficamente en el mapa. Aquí se guardan los datos del vuelo más relevantes para su representación. 

*PGTA: aquí se hallan todos los formularios del programa con los cuales se muestran las tablas y el mapa. También hay clases correspondientes con la representación gráfica.



Uso:
Para poder ejecutar este progama pulse pulse en  PGTA\PGTA.sln. Seguidamente se abrirá Visual Studio. Pulse el botón verde de Run (F5) y se ejecutará. 


Una vez se haya cargado un fichero (ya sea CAT 10 o CAT 21), tienes distintas formas de visualizar la tabla:

	-Puedes filtrar y obtener información sobre lo filtrado, pero utilizando esta opción solo podrás guardar en un archivo cvs de los datos que has filtrado
	
	-Puedes navegar por las páginas ya que el archivo es muy grande, teniendo la opción de guardar la página o todo el archivo.

Finalmente también existe la función de "Map View", la cual solo se abre si se ha cargado un archivo. Esta te deja visualizar el movimiento y la posición de los diferentes objetivos a distintas velocidades además de enseñarte los
datos del marker pulsado.

Este proyecto está llevado a cabo por Omar Abdel·lah Hossain y Joan Muñoz Sanchis