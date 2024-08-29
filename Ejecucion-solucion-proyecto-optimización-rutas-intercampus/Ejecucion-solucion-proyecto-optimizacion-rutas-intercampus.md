# Guía para Ejecutar solución e optimización de rutas para autobús intercampus ITM

## Abrir informe en blanco

1. **Abrir nuevo informe en blanco**

   - Abre la aplicación Power BI Desktop en tu computadora. Luego dar click en informe en blanco señalado en la imagen para iniciar un nuevo proyecto.
   - ![Informe en blanco](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/1-Abrir-informe-en-blanco-desktop.jpg)

2. **Obtener datos desde on origen web**

   - Una vez que Power BI Desktop esté abierto, y hayas seleccionado informe en blanco, verás en la barra de herramientas la opción "Obtener datos", esta opción es para conectar desde estos medios para obtener los datos necesarios.

  - Haz clic sobre esta opción y luego dentro de las subopciones haz clic en "web" en este caso la opción número 8 de forma descendente.
- ![Obtener datos - origen datos web](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/2-Obtener-datos-origen-web-desktop.jpg)

3. **Ingresar dirección URL**

   - Ingresa el siguiente link que tiene como para metros una serie de instrucciones seleccionadas para realizar una optimización dentro de varias opciones ofrecidas desde la API DE AZURE MAPS. 

[**LINK:**](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/link-origen-datos-API-azure.txt)   

  **NOTA:** Para entender un poco más sobre la parametrización del links y otros parámetros ajustables, por favor consulta la documentación de la API DE AZURE MAPS, [DOCUMENTACIÓN API AZURE MAPS](https://learn.microsoft.com/en-us/rest/api/maps/route/get-route-directions?view=rest-maps-2024-04-01&tabs=HTTP). 

- ![Ingreso URL - API AZURE MAPS](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/3-Insertar-direccion-URL-desktop.jpg)
  
   - Luego, haz clic en "Aceptar" y espera que se conecte y obtenga los datos.


4. **Editor avanzado - Modificar Power Query**

   - Luego del resultado anterior, sobre este mismo haz clic en "Editor avanzado".

![Editor avanzado - Power Query](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/4-Editor-avanzado-modificar-power-query-desktop.jpg)

   - Modifica el power query, es decir borra el actual y luego copia e ingresa al siguiente link para copiar el modificado.**Nota:** Verifica que la sintaxis esté correcta. [Power BI Query Modificado](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/PowerQuery.txt).

![Verificar sintaxis](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/4-Editor-avanzado-modificar-power-query-verificar-sintaxis-desktop.jpg)
   
   - Haz clic en Listo.

   - El resultado exitoso debe ser este resultado.

![Resultado exitoso - Power Query](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/4-Resultado-exitoso-power-query-latitud-longitud-tiempopromedio-velocidadpromedio-consumopromgasolina-ruta-desktop.jpg)

   - Luego haz clic en la esquina superior derecha, sobre "cerrar y aplicar", para continuar sobre el proceso.


5. **Carga de datos al modelo**


**Nota:**Debes esperar que se carguen los datos al modelo.

![Cargando-datos-al-modelo](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/5-Cargando-datos-al-modelo-desktop.jpg)


6. **Despliegue de modelado y modificación de tipo de formato para las variables**

   - Después de realizar el anterior proceso, despliega el modelado resultado para ver y modificar el formato de las variables

![Despliegue de modelado de datos](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/6-Despliegue-modelado-de-datos-para-modificar-tipo-formato-para-viarables-visualizacion-desktop.jpg).

   - Selecciona la variable Latitud, al seleccionar podrás ver en la parte superior que hay una sección llamada herramientas de columnas. Modifica el tipo de dato de la variable latitud por "Número decimal".

![Modificar de modelado de datos](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/6-Modificar-tipo-dato-latitud-desktop.jpg).

   - Luego debes confirmar el cambio de tipo de dato de la variable latitud. Haz clic en sí

![Confirmar cambio de tipo de dato](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/6-Confirmar-cambio-tipo-dato-latitud-desktop.jpg).

   - Luego debes modificar la categoría de la variable latitud, selecciona la correspondiente "latitud". Para saber si este proceso fue exitoso se debe visualizar el logo del hemisferio al lado de la variable al desplegar el modelado. Además deberás en la sección herramienta de "Resumen", debes darle "no resumir".

![Modificar categoría de dato](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/6-Modificar-categoria-y-no-resumir-dato-latitud-desktop.jpg).

   - Luego debes repetir el mismo proceso anterior para la variable longitud. 

![Modificar tipo y categoría variable longitud](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/6-Modificar-tipo-y-categoria-no-resumir-dato-longitud-desktop.jpg).


7. **Creación objeto visual - Mapa de Azure**

   - En la sección de visualizaciones, debes hacer clic sobre el logo de mapa de Azure, que luego parecerá en el tablero para creación de objetos visuales con sus datos.

![Mapa de azure](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/7-seleccion-mapa-azure-desktop.jpg)

  - Haz clic sobre el mapa de Azure y luego en la sección de datos chequear las variables: latitud, longitud y ruta. Las variables latitud y longitud mostraran las coordenadas de cada punto parte de cada ruta y la variable ruta distinguirá las diferentes rutas.

![Configurar mapa de azure](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/7-seleccion-mapa-azure-configura-variables-desktop.jpg)

- El resultado será el siguiente, puedes realizar modificaciones del texto, el tipo de mapa y entre otras cosas para una mejor visualización.

![ Resultado mapa de azure](https://github.com/sanrulo1030/Optimizacion-rutas-autobus-intercampus-ITM/blob/main/Ejecucion-solucion-proyecto-optimizaci%C3%B3n-rutas-intercampus/Imagenes/Desktop/7-resultado-azure-maps-desktop.jpg)
