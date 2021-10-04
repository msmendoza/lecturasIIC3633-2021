# Comentarios de Lectura: Semana 7

Esta semana al igual que el de la semana no dice relación directa con un algoritmo,
o framework en particular, sino que reúne diferentes técnicas de visualización
usadas en diferentes sistemas recomendadores. En particular se tocan tópicos
como transparencia, justificación, control, diversidad, _cold start_ e información
contextual (y novedad + _serendipity_, pero de manera más general al final del artículo),
y como es que la interacción con diferentes sistemas recomendadores interactivos,
mejora o empeora cada uno de estos aspectos.

De notable importancia encuentro la mención hacia _conversational AI_ a mediados
del documento, igualmente me hubiera gustado que el paper se expandiera más en
ese aspecto, dado los posibles frutos que esto podría traer. En particular un
bot bien entrenado, personalizado para determinado contexto, sería capaz de
disminuir en gran medida el problema de _cold start_ que tanto agobia a varios
métodos en este campo.

Si bien el impacto de interfaces interactivas para poder obtener información
contextual es alto dependiendo de las técnicas de visualización de datos en un
contexto dado, tenemos que la complejidad de uso de dichas interfaces debe
poder ser controlada por el usuario final para así poder tener un _match_ más
exacto con determinado segmento de clientes (tomemos el caso de TalkExplorer) y
que no aumente la desconfianza del sistema solo porque no es capaz de "comprenderse"
en su uso. Notemos como este aspecto aumentar en importancia al considerar
tecnologías emergente como las Smart Glasses que en menos de un año comenzarán
a invadir el mercado: claramente la abundancia de datos implícitos que podrán
ser extraídos de dichos dispositivos será enorme, pero a su vez hay que entender
que la forma en que estos se extraigan dependerá directamente de la técnica de
visualización de datos subyacente, y mucho mejor enfocado será este proceso
si el usuario es capaz de complejizar su interfaz hasta el grado donde se
sienta cómodo y pueda operar fluidamente en la plataforma.

Finalmente, como en otros papers se menciona el tema de _serendipity_ y _novelty_,
pero los autores no son claros al mencionar posibles direcciones en cuanto
a la medición de dichos factores en los sistemas recomendadores, por su puesto
es algo complejo de medir, pero igual lo extrañé en el documento.

**[1]** He, C., Parra, D., & Verbert, K. (2016). Interactive recommender
systems: A survey of the state of the art and future research challenges and
opportunities. Expert Systems with Applications, 56, 9-27.
