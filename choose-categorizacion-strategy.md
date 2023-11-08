<b>Contexto de la Decisión</b>

Dado que contamos con un sitio web que permite ofrecer paquetes turísticos diversos 
y que necesitamos añadirle la capacidad de categorizar múltiples experiencias dentro de los paquetes como por ejemplo la admisión de mascotas, aptitud para niños, disponibilidad de cabalgatas, late checkout, y otros atributos de índole muy variada pensamos en las implicancias que puede tener dotar al sistema de una categorización de paquetes mediante etiquetado (Tags). También viendo que al ir creciendo en su uso posiblemente tienda a ser difícil de gestionar, es importante garantizar que las etiquetas sean semánticamente coherentes y permitir la adición de nuevas etiquetas de manera controlada.

<b>Opciones de Solución Analizadas</b>

Se consideraron varias opciones para implementar la categorización de paquetes turísticos y el sistema de etiquetado:

Uso de Base de Datos Relacional: Se podría utilizar una base de datos relacional para almacenar información sobre los paquetes turísticos y las categorías de experiencias. Se crean tablas para cada tipo de categoría (por ejemplo, mascotas, niños, cabalgatas) y se asocian con los paquetes a través de FK.
Uso de Etiquetas Semánticas: En lugar de categorías rígidas, se podrían utilizar etiquetas semánticas para describir las características de los paquetes turísticos. Las etiquetas serían asignadas a los paquetes y podrían ser seleccionadas de un conjunto predefinido o añadidas de manera dinámica.
Algoritmo de Normalización de Etiquetas: Se podría implementar un algoritmo que normalice las etiquetas ingresadas por los usuarios para asegurarse de que las etiquetas sean semánticamente consistentes. Por ejemplo, "cabalgata" y "paseo a caballo" se mapearán a la misma etiqueta.
Sistema de Control de Etiquetas: Para controlar la proliferación de etiquetas y garantizar su coherencia semántica, se podría implementar un sistema de aprobación de etiquetas. Las etiquetas nuevas se agregan a una lista después de ser revisadas y aprobadas. A partir de ese punto, el usuario puede utilizarlas.

<b>Decisión Tomada</b>

<i>Estado: Aceptado</i>

Se decidió utilizar una combinación de las opciones 2, 3 y 4 para resolver los desafíos planteados:

Uso de Etiquetas Semánticas: Se utilizarán etiquetas semánticas para describir las características de los paquetes turísticos. Los usuarios podrán seleccionar etiquetas de un conjunto predefinido o agregar nuevas etiquetas de manera dinámica.

Algoritmo de Normalización de Etiquetas: Se implementará un algoritmo de normalización de etiquetas que mapeará etiquetas similares a una etiqueta única. Por ejemplo, "cabalgata" y "paseo a caballo" se mapearán a la misma etiqueta "cabalgata". Ver ejemplo de “cabalgata bajo la luz de la luna” creo que podría ser una combinación de tags.

Sistema de Control de Etiquetas: Se establecerá un sistema de control de etiquetas que permitirá la revisión y aprobación de nuevas etiquetas antes de ser agregadas a la lista general. Esto garantizará que las etiquetas sean semánticamente coherentes y evitamos la duplicación.

<b>Ventajas/Desventajas</b>

<b>Ventajas:</b>

<ul><li>Flexibilidad para los usuarios al seleccionar etiquetas.</li>
<li>Garantía de etiquetas semánticamente coherentes debido al algoritmo de normalización.</li>
<li>Control sobre el crecimiento desordenado/desmedido de etiquetas y la calidad de las mismas mediante el sistema de control de etiquetas.</li></ul>

<b>Desventajas:</b>

<ul><li>Requiere un proceso de revisión y aprobación para las nuevas etiquetas, lo que puede introducir demoras en su disponibilidad.</li>
<li>El algoritmo de normalización puede requerir ajustes surgidos de la experiencia de uso lo que puede tener un impacto en los paquetes previamente definidos.</li></ul>
