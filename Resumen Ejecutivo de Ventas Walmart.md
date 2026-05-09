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



