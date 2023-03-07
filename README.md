# Brecha Digital de Acceso en México

<img src="https://www.greengeeks.com/blog/wp-content/uploads/2020/04/Mobile-and-Desktop-Users.jpg" width=600 height=300>

*El proyecto sigue en contrucción pero se actualiza constantemente*

## Introducción

La Brecha Digital es una de las problemáticas con respesto a desigualdad más discutidas recientemente, y no es para menos,  
las TIC (Tecnologías de la Información y las Comunicaciones) se han convertido en una parte escencial de nuestra vida y como  
se desarrolla el mundo en general. El avance de las TIC ha sido acelerado y ha penetrado en varios aspectos tanto económicos   
como sociales, dando un valor especial al conocimiento y la información, lo que hizo que llamaran a este nuevo estadio de la  
sociedad como Sociedad de la Información. Y aunque a esta nueva "fase" de la sociedad las TIC estén siendo usadas en diversas   
partes, está distribución no es igual. No sólo en cuestiones de acceso, sino también en el uso y apropiación de estas mismas. 

En este análisis me enfocaré en la Brecha de Acceso y Uso, haciendo una comparación entres los usuarios de Computadoras y  
Smartphones en México. Partiré usando los Datos Abiertos de la Encuesta Nacional sobre Disponibilidad y Uso de Tecnologías de la  
Información en los Hogares (ENDUTIH) del 2021 hecha por el INEGI (Instituto Nacional de Estadística y Geografía). Este será un  
proyecto a largo plazo, así que se podría decir que está es la primera parte de los diversos análisis que se harán con respecto  
a la Brecha Digital.

## Datos

Los datos fueron obtenidos directamente del ENDUTIH 2021 en la página del INEGI en la sección de Datos Abiertos:  
https://www.inegi.org.mx/programas/dutih/2021/#Datos_abiertos

Todo bajo los TÉRMINOS DE LIBRE USO DE LA INFORMACIÓN DEL INEGI:   
https://www.inegi.org.mx/rnm/index.php/catalog/771

## Manejo de Datos

La base de Datos cuenta con 5 tablas independientes pero relacionales. No es obligatorio el juntar cada una de las tablas para   
los análisis, ya que estás se enfocan en ciertos indices diferenciados, como características socioedemográficas del hogar, de  
los residentes, condiciónes y características de las TIC tanto por hogar como por usuario.

El manejo de los datos por lo cual es simples de alguna manera, ya que los datos no viene etiquetados y sólo se etiquetarán  
aquellos que sean de uso para lás gráficas correspondientes. Para una referencia sobre el manejo de datos puede revisar el  
siguiente documento contenido en este repositorio:

[Manejo de Datos del ENDUTIH 2021](/jupyter_notebooks/1.1.-Data_Wrangling_ENDUTIH_2021.ipynb)

## Análisis de Datos

Las preguntas que se buscan responder son las siguientes.
¿Cuál es el acceso a las diferentes TIC de interés por hogar y por usuario?
¿Por qué no se tiene el mismo acceso, o cuales son las razones de ello según los residentes?

Y con ello vienen las siguientes preguntas

¿Qué diferencias hay entre los distintos usos de acuerdo al acceso de ciertos dispositivos?

### Acceso a TIC's en hogares mexicanos

Si te interesa saber el proceso de obtención y gráficado de datos puede revisar el siguiente documento que está ubicado en este  
repositorio:  
[Notebook de Acceso a TIC's en hogares mexicanos](/jupyter_notebooks/2.2.-Tics_households_Mexico.ipynb)

#### Panorama General del Acceso a TIC en los hogares

Es casi una obviedad pensar en cuál es la tecnología más extendida por todo el mundo; el Smartphone. Pero en este contexto se  
quiere  hacer una comparación entre los dispostivos con los cuales hay un interacción más directa con la internet, en específico  
con aplicaciones web o apps. Por eso mismo se comenzará el análisis comparando el acceso entre los hogares a Smartphones,  
Computadoras e Internet.

<img src="/Graphs/Tics_hog_sci.png" width=783 height=733>

Como se puede observar el acceso a los Smartphones es extendido comparado al internet en el hogar y especialmente a las  
computadoras. Entre más bajo se encuentre un hogar en el Estrato Socieconómico¹ menos acceso hay a Computadoras en gran medida,  
y también el acceso a Internet se reduce de una manera significativa. 
Esto es importante para futuros análisis, pues el acceso puede intervenir en el propio uso que se hace de internet.

**Prueba de chi cuadrado**:
Se hizo la prueba de hipótesis para comprobar que la distrbución de dispositivos no es aleatoria, y que la asociación entre  
variables es significante:

Valor p: 0.0001
Para más referencia revisar el documeto proporcionado.

#### Porqué no se tiene acceso a una computadora en el hogar

Dentro de la encuesta se enlista razones del porque no se tiene una computadora en casa, y esto es lo que se respondió en los
hogares:

<img src="/Graphs/NoComp_hog.png" width=1000 height=725>

Se puede observar cómo la principal razón es por falta de recursos económicos, seguida por la falta de interés y el no saber  
usar una computadora.
Esto hace notar que la problemática más grande en cuanto al acceso, tiene que ver con la falta de recursos económicos, el  
cual es un problema cruza por todos los ámbitos, y aquí no es la excepción.

