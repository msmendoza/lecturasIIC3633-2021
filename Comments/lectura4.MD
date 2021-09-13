# Content-Based Recommendation Systems

El paper trata sobre los sistemas recomendadores basados en contenido. En primera instancia,
se discuten los tipos de bases de datos, estructurados y no estructurados, y como vencer
complejidades aparentes en el caso no estructurado. Luego se analizan métodos para el
modelaje del perfil de usuario y finalmente se discuten limitaciones de los mismos, a la vez
que se introducen soluciones y específicamente, se toca el tema de la cooperación o complemento con
_collaborative filtering_ para resolver situaciones donde _content-based Filtering_ no es
capaz de realizar bien su tarea.

Encuentro bien explicado el proceso de _steamming_, al menos para mí, que desconocía
completamente el tema. De todas maneras quedo un tanto a la deriva cuando los autores
mencionan la desventaja de la pérdida de contexto al usar el procedimiento. Si bien,
ofrecen una alternativa al considerar términos continuos en lugar de una palabra aislada,
no hay mención alguna de si dicho proceso mitiga la desventaja.

Dentro de lo algoritmos expuestos para modelar las preferencias de usuario, Interesante
es el uso de Decision Trees. No conocía la aplicación de dicho modelo en este campo,
pero sin duda, su aplicación no solo permite modelar el interés de un usuario, sino
además generar un set de _if-then rules_, que finalmente termina por volver más
transparente el output del modelo. Esto fuertemente impacta en hacer conocer al
usuario el por qué de sus recomendaciones.

Finalmente, cierro el comentario destacando la importante relación expuesta en el
paper sobre content-based filtering y collaborative filtering en el sentido que el
primero puede funcionar como base para el segundo. De este modo se da paso al
desarrollo no de modelos tal vez complementarios, sino más bien mixtos en este
sentido.

**[1]** Pazzani, M. J., & Billsus, D. (2007). Content-based recommendation systems. In The adaptive web (pp. 325-341). Springer, Berlin, Heidelberg.
