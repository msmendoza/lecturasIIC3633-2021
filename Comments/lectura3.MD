# Evaluating recommendation systems

El paper trata sobre las diferentes propiedades que tienen los actuales sistemas
recomendadores, en particular no solo considerando elementos como la típica
_accuracy_ que siempre se usa para comparar modelos, sino elementos como
rapidez en la carga de las recomendaciones, diversidad en las mismas y tópicos
como la transparencia en la recomendación y la protección misma de los usuarios
desde el punto de vista de su privacidad. Se discuten además métricas de evaluación
y como concluir a partir de los resultados de los diversos experimentos, entre
ellos: experimentos offline, estudios de usuario y experimentos online.

Muy interesante el tópico tocado sobre el sesgo que podía aparecer al momento de
recolectar la data y a la vez el sesgo que se genera en ocasiones que los participantes
de un experimento no tienen el mismo peso en importancia como usuario, debido
más que nada a la historia misma del usuario y el peso de sus ratings, sin duda
es un elemento que yo no hubiera pensado o considerado en primera instancia.

Me parece extraño que dentro de las posibles _features_ cualitativas, posibles de
estimar en los _user studies_ y _online experiments_, no se haya considerado
o mencionado el posible ruido que estas variables son capaces de generar en la
predicción de rating o ranking de los mismos, llámese tiempo de clickeado al
llegar a cierta interfaz, tiempo en lograr una búsqueda, filtrados, etc.,
todo lo relacionado al comportamiento del usuario. En este aspecto, opino
necesario el uso de técnicas para seleccionar variables importantes relacionado
al análisis de _feature importances_ para realizar _feature selection_.

**[1]** Shani, G., & Gunawardana, A. (2011). Evaluating recommendation systems. In Recommender systems handbook (pp. 257-297). Springer, Boston, MA.
