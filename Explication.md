En este archivo se encuentra la investigación que he desarrollado con especto a la conexión entre SAP[^1] y las aplicaciones JAVA.


1. Como primer paso es neceario ir al portal de SAP para descargar e instalar el JCo[^2] en la computadora donde se ejecutará la aplicación JAVA. El JCo se puede descargar desde la página de soporte de SAP. Es muy importante asegurarse de que se está descargando la versión adecuada del JCo para la versión de SAP que se está utilizando. Una vez que se descargó será necesario descomprimir el archivo descargado en una ubicación adecuada en la computadora.

[^1]: SAP es uno de los principales productores mundiales de software para gestión de procesos de negocio, y desarrolla soluciones que facilitan el procesamiento eficaz de datos y el flujo de información entre las organizaciones.

[^2]: JCo (Java Connector) es un componente intermedio y una librería de desarrollo que permite a una aplicación Java comunicarse con SAP por medio de una RFC.

2. Utilizando el IDE (entorno de desarrollo integrado) donde se estárá trabajando el proyecto abriremos el Jco.

2.1. Ya en el proyecto se da clic con el botón derecho del mouse en la carpeta del proyecto en la que se desea incluir el archivo JCo.

<div align="center">

![image](https://github.com/JC-ULTRA/SAP-JAVA/assets/123017193/700136a6-c7e2-42e5-a1cc-d5836de9b12d)

</div>

2.2. En el menú que aparece con el clic derecho, hay que seleccionar la opción "Build Path" y luego "Configure Build Path".

<div align="center">

![image](https://github.com/JC-ULTRA/SAP-JAVA/assets/123017193/a7f1217b-701e-4d34-91db-0e48c4345827)

</div>

2.3 Ahora en la ventana de "Propiedades del proyecto", se debe seleccionar la pestaña "Librerías" y hacer clic en el botón "Agregar JARs...".

<div align="center">

![image](https://github.com/JC-ULTRA/SAP-JAVA/assets/123017193/f2a14387-6080-48d8-9033-3402b27115ed)

</div>

2.4 Debemos buscar el archivo JCo que se descargó y seleccionar para utilizar y hacer clic en "Aceptar" para agregar el archivo JCo al proyecto.


3. Una vez descargado en la ubicación se debe configurar la conexión en el archivo de la aplicación JAVA. Este archivo se puede encontrar en el directorio de la aplicación o en una ubicación específica para archivos de configuración el cual suele tener una extensión _".properties"_ o _".xml"_. Probablemente un archivo _".properties"_ podría componerse de los siguientes parametros:

```
sap.server.name=nombre_o_dirección_IP_del_servidor_SAP
sap.instance.number=número_de_instancia_de_SAP
sap.port.number=número_de_puerto_para_conectarse_a_SAP

```

E importar las clases JCoDestination[^3] & JCoException[^4] de la libreria en el código: 

```

import com.sap.conn.jco.JCoDestination;
import com.sap.conn.jco.JCoException;

```

Aunque cabe destacar que estos son solo ejemplos y los nombres reales de los parámetros varian de acuerdo al proyecto de negocio.

[^3]: JCoDestination se utiliza para representar una conexión a un sistema SAP, y se utiliza para enviar y recibir datos entre SAP y una aplicación Java

[^4]: JCoException se utiliza para manejar errores y excepciones que puedan ocurrir durante el proceso de conexión.
