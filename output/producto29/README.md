# DP29 - Cuarentenas Activas e Históricas: Descripción
Set de 3 archivos en formato csv y un archivo en formato GeoJSON que contiene la identificación y características de las zonas de cuarentena establecidas por el Plan de Acción por Coronavirus del Gobierno de Chile.

Las zonas de cuarentena se establecen como una medida sanitaria en una extensión territorial definida que implica que las personas deben permanecer en sus domicilios habituales hasta que la autoridad disponga lo contrario.

Los criterios para la definir la cuarentena son:

- Velocidad de Propagación de la Enfermedad
- Densidad de casos por km2
- Perfil etáreo de la población del territorio (adultos mayores y personas con enfermedades crónicas)
- Vulnerabilidad Social

Los archivos incluidos en el presente DP son:
- Cuarentenas-Activas.csv (Cuarentenas actualmente vigentes y futuras)
- Cuarentenas-Historicas.csv (Cuarentenas ya cumplidas incluyendo cambios dentro de una misma comuna)
- Cuarentenas-Totales.csv (Suma de cuarentenas vigentes, históricas y futuras)

# Columnas y valores

- Nombre: Nombre descriptivo de la zona de cuarentena.
- Estado: Valor codificado para estado de la cuarentena: Activa, No Activa, Futura, Sin Información.
- Alcance: Valor codificado para el alcance territorial de la cuarentena Comuna completa, Área Urbana Completa, Área Rural Completa, Sector Específico.
- Fecha de Inicio: Fecha y hora de inicio en tiempo UTC.
- Fecha de Término: Fecha y hora de término en tiempo UTC.
- Código CUT Comuna: Código Único Territorial de comuna asociada.
- Detalle: Observaciones adicionales al alcance de la cuarentena.
- Superficie en m<sup>2</sup>.
- Perímetro en m.

# Fuente
Plan de Acción del Gobierno de Chile para el COVID-19. Ver en: https://www.gob.cl/coronavirus/plandeaccion/

API Externa de Respaldo de Servicios para consulta. https://covid19.soporta.cl/datasets/0b944d9bf1954c71a7fae96bdddee464_1?geometry=-105.067%2C-44.515%2C-45.784%2C-32.531

Ejemplo de Uso: https://www.arcgis.com/apps/opsdashboard/index.html#/6d03fef7ffff4c7cbd11ef1e192e6bf2

# Frecuencia de actualización

Variable: días miércoles para cambios en áreas, días viernes para cambio de estado de las cuarentenas. Ocasionalmente se pueden decretar y activar cuarentenas en otras fechas

# Notas aclaratorias

**Nota aclaratoria 1:** La cartografía de delimitación de cuarentenas es de caracter referencial cuyos límites son obtenidos en base a fuentes oficiales para límites comunales y áreas urbanas

**Nota aclaratoria 2:** La definición territorial de la delimitación de cuarentenas está dada por la validación de distintas fuentes entre las que prima como criterio superior lo indicado por los Decretos en el Diario Oficial puesto que se encuentran diferencias sustantivas entre los mapas que muestran los distintos organismos de gobierno. Como criterio adicional para casos comunales se define la información y mapas proporcionados por los municipios e intendencias validada en acuerdo con las autoridades responsables de las medidas (Subsecretaría de Prevención del Delito y Jefatura de la Defensa Nacional de la correspondiente región)

# Notas de Versión

**19-06-2020**<br>
- Corrección de delimitación de cuarentena ID 90 (Curicó Urbano) en base a cartografía dispuesta por el Jefe de la Defensa Nacional Región del Maule

**18-06-2020**<br>
- Corrección de nombre de cuarentena ID 78 a Viña del Mar (CUT_COM 5109)
- Corrección de nombre de cuarentena ID 79 a Valparaíso (CUT_COM 5101)
- Se incorporan Cuarentenas decretadas en Res.Ex. MINSAL 467 del 17 de junio punto 2  (San Felipe, Los Andes, Rancagua, Machalí, Curicó Urbano)
- Se ajustan fechas de prórroga de cuarentenas en conformidad con punto 1 de la resolución antes mencionada

**12-06-2020**<br> 
- Cambio de Estado en Cuarentenas Futuras a Activas (9) 

**11-06-2020**<br> 
- En conformidad con Res.Ex. MINSAL 424 del 7 de junio se cambia la catergoría de la cuarentena ID 77 (Calama) de "Área Urbana Completa" a "Comuna Completa" modificando el área en el archivo GeoJSON
- Se incorporan Cuarentenas decretadas en Res.Ex. MINSAL 448 del 10 de junio punto 3.
- Se ajustan fechas de prórroga de cuarentenas
