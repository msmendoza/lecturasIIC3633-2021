# Comentarios de Lectura: Semana 5

Los papers de esta semana claramente no solo fueron escogidos basándose en el contenido
de la semana sino que también en cuanto a la relación entre ambos documentos. En **[1]**
se tiene una amplia discusión sobre la base de los _Context-Aware Recommender Systems_
(CARS), que añaden una dimensión de contexto a los ya conocidos pares usuario-item,
la definición de contexto, propiedades de los factores contextuales y paradigmas
de su uso. Por otra parte en **[2]**, a modo de complemento respecto de **[1]**
tenemos un paper de *ensemble learning* donde particularmente se demuestra la superioridad
de los algoritmos de blending no tradicionales propuestos por los autores en
contraposición con la regresión lineal tradicional del _linear blending_.

Hablo de complemento, puesto que en **[1]** cuando se habla de los paradigmas, tenemos
que una de las muchas maneras que hay para extraer riqueza de la nueva dimensión de
contexto está suponer varios de ellos, modelar de acuerdo a ello y finalmente ponderar
(en una perspectiva de paradigma _contextual modeling_) las recomendaciones de los
diferentes modelos para así dar la recomendación final. Sin duda, muchos de los
_blendings_ mencionados en **[2]** podrían ser usados en problemas con input (usuario,
item, contexto), pero para encontrar el algoritmo de _blending_ particular, se requiere
hacer un estudio primero de las promesas del algoritmo, cotas de complejidad
y ámbito de uso. Notemos como todo los problemas de duración de tiempo de entrenamiento,
límite de datos en memoria y tiempo de predicción vistos en **[2]** son capaces de
empeorar rápidamente a causa de esta nueva dimensión de contexto.

Respecto de la escritura de ambos papers, me pareció demasiado clara, sobre todo
en términos de los algoritmos/modelos discutidos. En **[2]**, el resumen es conciso y
preciso, destaco y agradezco de todas maneras la importancia en la explicación
de las complejidades de entrenamiento, predicción y uso de memoria. Es muy fácil o
natural a veces aprender algortimos e implementarlos en el campo de Machine Learning,
pero no siempre se tienen en cuenta dichos factores, en ese sentido me hizo replantearme
el aprendizaje de los modelos vistos en el ramo hasta el momento.

En **[1]** la lectura fue fluida gracias a completos ejemplos que ofrecieron los autores
para cada uno de los tópicos tocados, destaco de este paper dos cosas: el paradigma
de Prefiltrado, pues me parece osado el hecho de usar sensores de celulares por ejemplo,
para obtener data contextual que permita al sistema discriminar datos relevantes
dentro del dataset de ratings, esto tiene efectos en la complejidad total del algoritmo
(respecto de su reducción), pero su implementación no me parece nada trivial, tal vez
extrañe un poco de eso en el paper. Y por otra parte, el posible ensamblaje que
se puede dar para sortear el hecho de que aún no contamos con una definición clara
de contexto (en investigación) y como es que este varía para cada caso de uso,
así, claro, se puede construir algo robusto en cuanto a precisión en las recomendaciones,
pero se pierde otra parte harto tiempo de entrenamiento al tener que recurrir
al ensamblaje de modelos. Seguramente, una perspectiva más novedosa de ello
lograría sacar a la comunidad del hoyo actual respecto a CARS.


**[1]** Adomavicius, G., Mobasher, B., Ricci, F. and Tuzhilin, A. (2011). Context-Aware Recommender Systems. AI Magazine, 32(3), 67-80.

**[2]** ahrer, M., Töscher, A. and Legenstein, R. (2010). Combining predictions for accurate recommender systems. In Proceedings of the 16th ACM SIGKDD International Conference on Knowledge Discovery and Data Mining, 693-702. ACM.
