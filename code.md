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