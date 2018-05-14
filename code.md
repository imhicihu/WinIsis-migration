
 	
     Diálogo de Importación	Ayuda en Línea de WinIsis


Contenido del Capítulo

  Resumen 
  Nombre del archivo ISO de entrada
  Primer MFN a ser asignado
  Campo con MFN 
  FST de Reformateo 
  Tabla de Conversión Gizmo 
  Longitud de la línea de entrada 
  Separador de Subcampos 
  Opciones

  Tabla de Contenido

Resumen	Ayuda en Línea de WinIsis


La Ventana de diálogo de importación se despliega en respuesta al comando Importar del menú Base de Datos. Al seleccionar dicho comando aparece primero la correspondiente ventana de diálogo abrir:

Presione sobre los elementos de la imágen que sigue para obtener una descripción detallada de cada tema.


 


en la que se seleccionará el archivo *.iso que se desea importar. Tras ello se despliega la siguiente ventana.

 

Nombre del archivo ISO de entrada

Este campo contiene el nombre de archivo que se eligió en la ventana de Archivo ISO de entrada. El Archivo debe estar en el formato estándar ISO 2709 descrito en el Manual de Referencia de CDS/ISIS. 

Primer MFN a ser asignado

Si se especifica este parámetro CDS/ISIS renumerará secuencialmente los registros de entrada a partir del número de MFN especificado. Normalmente se debe introducir 1 si se está usando la opción Cargar, y el número de registros actual de la base + l, cuando se usan las opciones Añadir o Actualizar. En este último caso, sin embargo, si se indica un número de registro (MFN) ya asignado a un registro presente en la base de datos, CDS/ISIS numerará automáticamente los registros importados a partir del próximo número de registro a ser asignado en la base (por tanto las opciones Añadir y Actualizar funcionan de la misma forma).

Campo con MFN 

Como alternativa a la opción anterior (que será ignorada en caso de especificar una etiqueta de entrada), puede asignarse el MFN a partir de un campo del registro de entrada. En este caso, el usuario especifica en este campo la etiqueta ISO del campo que contiene el MFN. Nótese que el campo debe contener un valor numérico, y sólo puede usarse para este propósito, ya que no será almacenado en los registros de la base de datos receptora.

FST de Reformateo 

Este parámetro es opcional. Si se deja en blanco, los campos en el archivo de salida mantendrán sus etiquetas y su contenido. En forma alterna, puede realizarse cierto grado de reformateo suministrando el nombre de una FST.
Cuando se usa para reformateo, la FST se interpreta de la manera siguiente:
Cada línea de la FST representa un campo de salida;
A cada campo de salida se le asigna una etiqueta igual al identificador de campo definido en la línea correspondiente de la FST.
El formato de extracción de datos incluido en la FST define el contenido del campo. En este formato, se deben usar las etiquetas ISO de los campos según se definieron para el archivo de entrada. Cada línea producida por el formato (o cada elemento, si la FST especifica las técnicas de indizado 2, 3 o 4) generará una nueva ocurrencia del campo de salida. Nótese que el archivo de palabras vacías de la base de datos receptora, si lo hay, será usado para procesar los campos con técnica de indizado 4.

Supóngase por ejemplo que el archivo de entrada contiene los campos siguientes:
100 Autor (repetible)
200 Título
300 Palabras clave (repetible)
400 Notas

Una FST para reformateo para este archivo podría ser la siguiente:
1 0 (v100/) [campo de salida 1 igual al campo de entrada 100]

2 0 v200 [campo de salida 2 igual al campo de entrada 200]

3 0 |<|v300|>| [campo de salida 3 contiene las palabras clave encerradas entre
                      <..>; cada palabra clave será tomada de una ocurrencia del campo
                      de entrada 300] 