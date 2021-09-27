# Comentarios de Lectura: Semana 6

El paper de esta semana no es sobre un algoritmo o framework en particular
sino más bien una revisión de literatura sobre sistemas de recomendaciones
basados en Deep Learning. La estructura del paper es más bien amena para la
cantidad de información y complejidad de lo que se trata, en primer lugar
tenemos una breve descripción de la mayoría de técnicas de Deep Learning usadas
en el campo de recomendación, luego una serie de justificaciones sobre por qué
es factible usar técnicas de DL en sistemas de recomendación, esto acompañado
después de las falencias que la comunidad actualmente encuentra en el uso de
dichos algoritmos.

Destaco dentro de los pros de usar DL en sistemas recomendadores el hecho de
poder atacar situaciones en las cuales los datos vienen en forma de una
"serie de datos" (_time series_), lo cual nos permite tener sistemas robustos
frente a escenarios como recomendaciones por sesión o recomendaciones
adaptativas a medida que se va llenando un carro o armando una _playlist_. En
este sentido, de alto impacto son los métodos que involucran RNNs dado que
estas redes son bien conocidas por poder capturar dependencias temporales
(a veces dinámicas) entre diferentes registros de datos.

Respecto a los cons del uso de DL, me encuentro con las típicas críticas en base
a transparencia, cantidad de datos y lo costoso que es la etapa de
_hyperparameter tuning_. Tal vez hubiera esperado que a lo largo del documento
los autores hubieran podido evidenciar de manera más explícita el como suplir
los problemas de transparencia e interpretabilidad de las recomendaciones,
en particular solo referencian a artículos asociados además de comentar el
aspecto casi obvio de que es bastante complejo interpretar una predicción
mirando solamente el peso asignado finalmente a determinada neurona.

Hago el alcance anterior porque desde la experiencia propia hago investigación
en el campo de criminología donde también se utilizan, dependiendo de contexto,
técnicas de Machine Learning o Deep Learning, así, la predicción espacio-
temporal de incidentes, tiene que (o debe intentar) ser lo más transparente
posible para así evitar posibles problemas como son la predicción sesgada
de tipo racial, por localidad u otros indicadores demográficos. En este sentido
se suelen usar complementar los frameworks con _if-then models_ en alguna
parte de la arquitectura para así poder explicar de alguna forma el por qué de
la predicción, o bien enriquecer los datos de input utilizando una gran cantidad
de información contextual del entorno que rodea a cada celda una grilla de ciudad
(como visto en **[2]**).

Finalmente, se discute el estado de arte y la taxonomía realizada por autores
para clasificar los algoritmos. La clasificación es clara, pero se evidencia
que el paper es para un público especializado, pues desconocía la gran mayoría
de los frameworks enunciados y solo conocía la base de los mismos, elementos
como CNN, RNN, MLP, etc. Ávido estoy por querer conocer el impacto de los
CNNs en el ámbito de _feature extraction_ para sistemas recomendadores. Hasta
el momento solo conocía su uso en procesamiento de imágenes y grillas de ciudades
para capturar patrones de delincuencia, pero sin duda el impacto en este campo
es mucho más rico, como menciona el documento, al permitir incluir datos como
imágenes y texto, no solo estático sino también secuencial.


**[1]** Zhang, S., Yao, L., Sun, A., & Tay, Y. (2019). Deep learning based recommender system: A survey and new perspectives. ACM Computing Surveys (CSUR), 52(1), 1-38.

**[2]** Wheeler, A. P., & Steenbeek, W. (2021). Mapping the risk terrain for crime using machine learning. Journal of Quantitative Criminology, 37(2), 445-480.
