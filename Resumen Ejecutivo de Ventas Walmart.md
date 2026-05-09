https://docs.google.com/spreadsheets/d/1wnLBjDlJ_NY4dBWBa2UR-FisdTJ2sv1EXWQpxY7n8NY/edit?usp=sharing

Los objetivos del proyecto fueron:  

    Preparar datos para el análisis (limpieza, enriquecimiento, documentación).  
    Construir KPIs clave para evaluar la eficiencia y la participación.  
    Crear dashboards dinámicos con filtros y visualizaciones útiles para los stakeholders.  
    Comunicar hallazgos ejecutivos mediante el método C→F→I.  
    Aplicar QA para asegurar la calidad y trazabilidad del análisis.

1.- LIMPIAR: preparar los datasets para su análisis.

Copié la hoja raw_ventas y la renombré clean_ventas, marcando esta pestaña en verde.
<img width="480" height="36" alt="image" src="https://github.com/user-attachments/assets/d74f902f-0c2d-4801-82d4-f936404096c7" />
<br>
Normalicé columnas ( Fecha, ventas_semanales).  
Fecha: Aseguré formato de fecha.  
ventas_semanales: Aseguré formato $ xxxx.xx (por ejemplo, $ 1005.05)

Salida esperada: la hoja ventas_clean lista para su análisis con las columnas: tienda | Dept | Fecha | ventas_semanales | esferiado | semana_limpia.
<img width="620" height="222" alt="image" src="https://github.com/user-attachments/assets/3e3f743d-e48f-4afc-b50e-da46cfd98f4d" />
<br>
2.- Enriquecimiento

Añadí a clean_ventas las columnas tipo, tamaño, nombre_dept desde los otros datasets (raw_tiendas, raw_departamento, raw_ventas), con el fin de calcular la eficiencia y crear reportes legibles.

Esto mediante

=BUSCARV(valor_buscado; rango_tabla; índice_columna; FALSO)  

Salida esperada: tabla consolidada con todas las columnas clave: tienda | Dept | Fecha | ventas_semanales | esferiado | semana_limpia| tipo | tamaño | nombre_dept.
<img width="984" height="236" alt="image" src="https://github.com/user-attachments/assets/34037c5c-7236-4a3f-8df0-8808ba895acb" />
<br>
3.- Resumen con tablas dinámicas  

Construí una tabla dinámica para cada KPI.

Por qué: Las tablas resumen fueron la fuente para un Dashboard dinámico.

3.1 KPI 1: Ventas por m²  

3.1.1 Creé una tabla agrupada por departamento que contiene:  

    Suma de ventas semanales del 2012.  
    Promedio del tamaño.  

3.1.2 Agregué un campo calculado:  

    ventasxmetro2, el cual se obtuvo con la instrucción:  
    =SUMA(ventas_semanales) / AVERAGE(tamaño)  


3.1.3 Filtré por las ventas exclusivamente del año 2012  

    Añadí un filtro:  Mostrar solo las filas en la columna semana_limpia que contenga el texto: 2012  
    
Salida esperada: Tabla dinámica con 4 columnas: nombre_dept, SUM of ventas_semanales, AVERAGE of tamaño y ventasxmetro2
<img width="604" height="335" alt="image" src="https://github.com/user-attachments/assets/5b93020c-a9b6-48f4-a4fe-ce0254a603c9" />
<br>
3.2 KPI 2: Participación por departamento  

3.2.1 Creé una tabla agrupada por departamento que contiene:  

    Suma de ventas semanales por departamento en el 2012 mostradas como un % del total.  
    
3.2.2 Filtré por las ventas exclusivamente del año 2012  

    Añadí un filtro:  Mostrar solo las filas en la columna semana_limpia que contenga el texto: 2012  
<img width="376" height="336" alt="image" src="https://github.com/user-attachments/assets/c8d17f48-02b2-4ba2-bafb-56b31d555cc0" />
<br>
4.- Dashboard  

El dashboard es la hoja donde los diferentes stakeholders pueden filtrar por su departamento y ver sus KPIs al instante.  

4.1 Creé una celda de selección (entrada del usuario) donde con un menú desplegable asigné los nombres de los departamentos.  
<img width="255" height="111" alt="image" src="https://github.com/user-attachments/assets/72ddde93-0973-4046-b6fd-5cec5ae408aa" />

4.2 Trajé los KPIs al dashboard para enlazar la selección (nombre departamento)  

    Utilicé  
    VLOOKUP/BUSCARV 

4.2.1 Asigné el nombre Ventas x metro cuadrado a un conjunto de celdas combinadas donde debajo de él devulve el valor de la columna ventasxmetro2.  

4.2.2 Asigné el nombre Participación por departamento a un conjunto de celdas combinadas donde debajo de él devulve el valor de la columna SUM of ventas_semanales.  
<img width="1164" height="160" alt="image" src="https://github.com/user-attachments/assets/9b46afae-c51e-4f37-a183-019c67d5523d" />  
<br>  
4.3 Formato de los KPIs  

Utilicé un formato condicional para resaltar los valores (por ejemplo: participación menor a 5% en rojo).
<img width="1353" height="205" alt="image" src="https://github.com/user-attachments/assets/215525c0-ed03-4279-82c8-779457759bb8" />
<br>  
4.4 Visualizar los KPIs  
<br>  
4.4.1 KPI 1: Ventas por metro cuadrado  
  
Creé un gráfico de barras que muestra ventas/m² por departamento, ordenando la tabla dinámica de mayor a menor para que las barras se muestren en ese orden y resalten la eficiencia.
<img width="496" height="496" alt="image" src="https://github.com/user-attachments/assets/a8810223-75f4-482a-a4ed-3e7e73d0f403" />  
4.4.2 KPI 2: Participación del Departamento  
  
Creé un gráfico de barras apiladas que muestra la proporción de cada departamento sobre el total de ventas. Cada departamento tiene un color distinto, así poder ver no solo la participación individual, sino también la comparación con otros.
<img width="713" height="498" alt="image" src="https://github.com/user-attachments/assets/f8f37137-3609-422d-b80f-ad5b2013075e" />  
5.- Resumen ejecutivo (C → F → I)  

En una hoja de cálculo extra llamada Resumen, redacte un informe ejecutivo corto y accionable que responde las 2 preguntas de negocio usando el método Context → Finding → Implication (C→F→I).
Cada respuesta debe incluye evidencia (una visualización) que la respalda.  
<img width="817" height="363" alt="image" src="https://github.com/user-attachments/assets/4fb19882-cce0-42df-9a10-edcce272504e" />  

<img width="506" height="580" alt="image" src="https://github.com/user-attachments/assets/2f7a745a-09be-4026-ada2-5de8ea9a6111" />  
  
6.- QA (Quality Assurance)  

Creé una hoja de cálculo extra llamada Readme donde:  

    Documenté el proyecto y verifiqué la integridad y exactitud de los datos, los cálculos y el dashboard.  
    Documenté las comprobaciones, resultados y acciones tomadas en la hoja.

Por qué: Para que cualquier compañero pueda entender qué contiene el archivo y cómo lo construí.

<img width="1082" height="634" alt="image" src="https://github.com/user-attachments/assets/20c7034e-2a93-4e21-8828-9898456c64b2" />  











 


