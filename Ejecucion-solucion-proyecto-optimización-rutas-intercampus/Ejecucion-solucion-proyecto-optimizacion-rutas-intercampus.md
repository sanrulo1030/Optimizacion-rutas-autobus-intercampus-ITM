# Guía para Ejecutar solución e optimización de rutas para autobús intercampus ITM

## Abrir informe en blanco

1. **Abrir nuevo informe en blanco**

   - Abre la aplicación Power BI Desktop en tu computadora. Luego dar click en informe en blanco señalado en la imagen para iniciar un nuevo proyecto.
   - ![Informe en blanco](#) [Enlace para imagen de Power BI Desktop abriéndose]

2. **Obtener datos desde on origen web**

   - Una vez que Power BI Desktop esté abierto, y hayas seleccionado informe en blanco, verás en la barra de herramientas la opción "Obtener datos", esta opción es para conectar desde estos medios para obtener los datos necesarios.

  - Haz clic sobre esta opción y luego dentro de las subopciones haz clic en "web" en este caso la opción número 8 de forma descendente.
- ![Obtener datos - origen datos web](#) [Enlace para imagen de botón "Iniciar sesión" en Power BI Desktop]

3. **Ingresar dirección URL**

   - Ingresa el siguiente link que tiene como para metros una serie de instrucciones seleccionadas para realizar una optimización dentro de varias opciones ofrecidas desde la API DE AZURE MAPS. 

**LINK:**  
-  https://atlas.microsoft.com/route/directions/json?api-version=1.0&query=6.27555,-75.58816:6.24546,-75.54991&maxAlternatives=4&subscription-key=27nYcegxljPpPq0IuNzWJ7D4hognyjdlgZCy0LovJljzAbLH2EEeJQQJ99AEACYeBjF7S6WmAAAgAZMPObOT&departAt=2024-06-14T17:00:00-05:00&constantSpeedConsumptionInLitersPerHundredkm=40,17

  **NOTA:** Para entender un poco más sobre la parametrización del links y otros parámetros ajustables, por favor consulta la documentación de la API DE AZURE MAPS, [DOCUMENTACIÓN API AZURE MAPS](https://learn.microsoft.com/en-us/rest/api/maps/route/get-route-directions?view=rest-maps-2024-04-01&tabs=HTTP). 

   - Luego, haz clic en "Aceptar" y espera que se conecte y obtenga los datos. El resultado dará lo siguiente si es exitoso.

![Resultado](#) [Enlace para imagen resultado obtención de datos]


4. **Editor avanzado - Modificar Power Query**

   - Luego del resultado anterior, sobre este mismo haz clic en "Editor avanzado".

![Editor avanzado - Power Query](#) [Enlace para imagen de ingreso de Power query modificado - verificar sintaxis]

   - Modifica el power query, es decir borra el actual y luego copia e ingresa el siguiente link para copiar el modificado.**Nota:** Verifica que la sintaxis esté correcta. [Power BI Query Modificado](https://app.powerbi.com).
   
   - Haz clic en Listo.

![Verificar sintaxis](#) [Enlace para imagen de ingreso de Power query modificado - verificar sintaxis]

   - El resultado exitoso debe ser este resultado.

![Resultado exitoso - Power Query](#) [Enlace para imagen de ingreso de Power query modificado - verificar sintaxis]

   - Luego haz clic sobre "cerrar y aplicar", para continuar sobre el proceso.

![Cerrar y aplicar resultado](#) [Enlace para imagen de ingreso de Power query modificado - verificar sintaxis]

5. **Carga de datos al modelo**


**Nota:**Debes esperar que se carguen los datos al modelo.

![Cargando-datos-al-modelo](#) [Enlace para imagen de ingreso de Power query modificado - verificar sintaxis]


6. **Despliegue de modelado y modificación de tipo de formato para las variables**

   - Después de realizar el anterior proceso, despliega el modelado resultado para ver y modificar el formato de las variables

![Despliegue de modelado de datos](#) [Enlace para imagen de Power BI Desktop listo para usarse].

   - Selecciona la variable Latitud, al seleccionar podrás ver en la parte superior que hay una sección llamada herramientas de columnas. Modifica el tipo de dato de la variable latitud por "Número decimal".

![Modificar de modelado de datos](#) [Enlace para imagen de Power BI Desktop listo para usarse].

   - Luego debes confirmar el cambio de tipo de dato de la variable latitud. Haz clic en sí

![Confirmar cambio de tipo de dato](#) [Enlace para imagen de Power BI Desktop listo para usarse].

   - Luego debes modificar la categoría de la variable latitud, selecciona la correspondiente "latitud". Para saber si este proceso fue exitoso se debe visualizar el logo del hemisferio al lado de la variable al desplegar el modelado. Además deberás en la sección herramienta de "Resumen", debes darle "no resumir".

![Confirmar cambio de categoría de dato](#) [Enlace para imagen de Power BI Desktop listo para usarse].

   - Luego debes repetir el mismo proceso anterior para la variable longitud. 

![Modificar tipo y categoría variable longitud](#) [Enlace para imagen de Power BI Desktop listo para usarse].


6. **Creación objeto visual - Mapa de Azure**

   - En la sección de visualizaciones, debes hacer clic sobre el logo de mapa de Azure, que luego parecerá en el tablero para creación de objetos visuales con sus datos.

![Mapa de azure](#) [Enlace para imagen de Power BI Desktop listo para usarse]

  - Haz clic sobre el mapa de Azure y luego en la sección de datos chequear las variables: latitud, longitud y ruta. Las variables latitud y longitud mostraran las coordenadas de cada punto parte de cada ruta y la variable ruta distinguirá las diferentes rutas.

![Configurar mapa de azure](#) [Enlace para imagen de Power BI Desktop listo para usarse]

- El resultado será el siguiente, puedes realizar modificaciones del texto, el tipo de mapa y entre otras cosas para una mejor visualización.

![ Resultado mapa de azure](#) [Enlace para imagen de Power BI Desktop listo para usarse]
