# Brecha Digital de Acceso en México, diferencias entre el acceso a Smartphones y Computadoras.

<img src="https://www.greengeeks.com/blog/wp-content/uploads/2020/04/Mobile-and-Desktop-Users.jpg" width=600 height=300>

*El proyecto sigue en contrucción pero se actualiza constantemente*

## Tabla de Contenidos
- [Introducción](#0)
- [Datos](#1)
- [Manejo de Datos](#2)
- [Conceptos](#3)
- [Análisis de Datos](#4) 
  - [Acceso a TIC's en hogares mexicanos](#5)
    - [Panorama General del Acceso a TIC's en los hogares](#6)
    - [Porqué no se tiene acceso a una computadora en el hogar](#7)
  - [Usuarios de TIC's en México](#8)
    - [Usuarios de TIC's por Estrato Socioeconómico](#9)
    - [Desde que lugar acceden más a internet los usuarios](#10)

## Introducción <a id="0"></a>

La Brecha Digital es una de las problemáticas con respesto a desigualdad más discutidas recientemente, y no es para    
menos, las TIC (Tecnologías de la Información y las Comunicaciones) se han convertido en una parte escencial de  
nuestra vida y como se desarrolla el mundo en general. El avance de las TIC ha sido acelerado y ha penetrado en  
varios aspectos tanto económicos como sociales, dando un valor especial al conocimiento y la información, lo que  
hizo que llamaran a este nuevo estadio de la sociedad como Sociedad de la Información. Y aunque a esta nueva  
"fase" de la sociedad las TIC estén siendo usadas en diversas partes, está distribución no es igual. No sólo en  
cuestiones de acceso, sino también en el uso y apropiación de estas mismas. 

En este análisis me enfocaré en la Brecha de Acceso y Uso, haciendo una comparación entres los usuarios de  
Computadoras y Smartphones en México. Partiré usando los Datos Abiertos de la Encuesta Nacional sobre  
Disponibilidad y Uso de Tecnologías de la  Información en los Hogares (ENDUTIH) del 2021 hecha por el INEGI  
(Instituto Nacional de Estadística y Geografía). Este será un proyecto a largo plazo, así que se podría decir  
que está es la primera parte de los diversos análisis que se harán con respecto a la Brecha Digital.  

## Datos <a id="1"></a>

Los datos fueron obtenidos directamente del ENDUTIH 2021 en la página del INEGI en la sección de Datos Abiertos:  
https://www.inegi.org.mx/programas/dutih/2021/#Datos_abiertos

Todo bajo los TÉRMINOS DE LIBRE USO DE LA INFORMACIÓN DEL INEGI:   
https://www.inegi.org.mx/rnm/index.php/catalog/771

## Manejo de Datos <a id="2"></a>

La base de Datos cuenta con 5 tablas independientes pero relacionales. No es obligatorio el juntar cada una de las   
tablas para los análisis, ya que estás se enfocan en ciertos indices diferenciados, como características  
socioedemográficas del hogar, de los residentes, condiciónes y características de las TIC tanto por hogar como   
por usuario. El manejo de los datos por lo cual es simples de alguna manera, ya que los datos no viene etiquetados  
y sólo se etiquetarán aquellos que sean de uso para lás gráficas correspondientes. Para una referencia sobre el   
manejo de datos puede revisar el siguiente documento contenido en este repositorio:

[Manejo de Datos del ENDUTIH 2021](/jupyter_notebooks/1.1.-Data_Wrangling_ENDUTIH_2021.ipynb)

## Conceptos <a id="3"></a>

Se puede sobreentender lo que se quiere análizar aquí, pero es importante dejar en claro, cuál es el significado de los conceptos usados, o al menos dejar claro los básicos para un mejor entendimiento. Tanto de manera general como para términos de la propia Base de Datos. A countinuación enlistaré los conceptos que requieren esa conceptualización.

- **Brecha Digital:** Cito textualmente: “la brecha entre individuos, hogares, negocios y áreas geográficas en diferentes niveles socioeconómicos con respecto a sus oportunidades de acceso a tic y su uso para una amplia variedad de actividades” (OECD, 2001, como se citó en Navarro, López, Domínguez, & Castañeda, 2018).

- **Brecha Digital de Acceso:** Dentro de la Brecha Digital existen varias dimensiones, y para esto se usa la distición según el modelo que hace Selwyn (2004): "el acceso, incluye el acceso formal relacionado con la disponibilidad de tic en hogares, escuelas y comunidades para ser utilizadas por todos, así como el acceso efectivo vinculado con la disponibilidad de tic en hogares, escuelas y comunidades para ser utilizadas por quienes consideran que pueden hacerlo" (como se citó en Navarro, López, Domínguez, & Castañeda, 2018).

- **Estrato Socioeconómico**: El INEGI elaboró sus propios estratos (cuatro) a partir de medios propios y van más allá del salario que obtienen los hogares, aquí está la descripción: "… esta estratificación considera las características sociodemográficas de los habitantes de las viviendas, así como las características físicas y el equipamiento de las mismas, expresadas por medio de 34 indicadores construidos con información del Censo de Población y Vivienda 2010, para lo cual se emplearon métodos estadísticos multivariados" (INEGI, 2021).

- **Hogar**: "Conjunto formado por una o más personas, unidas o no por lazos de parentesco, que residen habitualmente en la misma vivienda particular y se sostienen de un mismo gasto para la alimentación" (INEGI, s.f.).

- **Usuario de Computadora**: "Individuo de 6 años o más que tiene el conocimiento o habilidad necesaria para que, de manera autónoma, encienda, realice alguna actividad en la computadora y la apague. Las actividades pueden ser de carácter escolar, que atiendan situaciones laborales, como medio de comunicación, de entretenimiento, de compra o pago de bienes y servicios, entre otros" (INEGI, s.f.).

- **Usuario de Internet**: "Individuo de 6 años o más que en forma eventual o cotidiana, y de manera autónoma, ha accedido y realizado alguna actividad en Internet en los últimos doce meses. Las actividades pueden ser, entre otras, para realizar tareas escolares; las relacionadas con el trabajo; de comunicación, incluyendo correos electrónicos o conversaciones escritas (Chat); de capacitación, adiestramiento o formación a distancia mediante videoconferencias; de entretenimiento, como son las de bajar o jugar videojuegos o programas de computadora en la red, como son los de música" (INEGI, s.f.).

- **Usuario de Telefonia celular**: "Individuo de 6 años o más de edad que de manera autónoma se comunicó con otra persona mediante un teléfono celular, durante los últimos tres meses, ya sea como emisor o receptor de una llamada. Incluye envío o recepción de mensajes, así como consulta de información. El uso de un teléfono celular implica que la persona tiene el aparato a su disposición, independientemente de la propiedad del mismo o de quién pague el servicio" (INEGI, s.f.).

## Análisis de Datos <a id="4"></a>

Las preguntas que se buscan responder son las siguientes.  

- **¿Cuál es el acceso a las TIC's de interés en los hogares mexicanos por Estrato Socioeconómico?** 
- **¿Razones por las cuáles ese acceso es desigual?** 

- **¿Cuál es la medida de usuarios que hay por TIC a partir de su Estrato Socioeconómico?** 
- **¿Cuáles son las razones de esa diferencias en el acceso o uso de las TIC's?**
 

### Acceso a TIC's en hogares mexicanos <a id="5"></a>

Si te interesa saber el proceso de obtención y gráficado de datos puede revisar el siguiente documento que está  
ubicado en este repositorio:  
[Notebook de Acceso a TIC's en hogares mexicanos](/jupyter_notebooks/2.2.-Tics_households_Mexico.ipynb)

#### Panorama General del Acceso a TIC's en los hogares <a id="6"></a>

Es casi una obviedad pensar en cuál es la tecnología más extendida por todo el mundo; el Smartphone. Pero en  
este contexto se quiere  hacer una comparación entre los dispostivos con los cuales hay un interacción más  
directa con la internet, en específico con aplicaciones web o apps. Por eso mismo se comenzará el análisis  
comparando el acceso entre los hogares a Smartphones, Computadoras e Internet.

![Acceso a tics por hogar](/Graphs/Tics_hog_sci.png)

Como se puede observar el acceso a los Smartphones es extendido comparado al internet en el hogar y especialmente a las computadoras. Entre más bajo se encuentre un hogar en el Estrato Socieconómico menos acceso hay a Computadoras:
- Estrato Socioeconómico Alto: 76.43%
- Estrato Socioeconómico Medio Alto: 57.67%
- Estrato Socioeconómico Medio Bajo: 36.25%
- Estrato Socioeconómico Bajo: 13.49%

Esto marca una clara diferencia entre el acceso a una computadora, y es diferente al acceso de los Smartphones, pues sus proporciones se mantiene más estables.

También es el caso del acceso a Internet, aunque no tan marcado como el acceso a computadoras:
- Estrato Socioeconómico Alto: 92.08%
- Estrato Socioeconómico Medio Alto: 83.56%
- Estrato Socioeconómico Medio Bajo: 66.34%
- Estrato Socioeconómico Bajo: 34.03%

Este acceso a las TIC's en el hogar no es algo que marque puntualmente si acceden o no a cualquiera de estas, pues no todos los miembros del hogar pueden acceder a estos dispositivos, además este no se limita al hogar, pues puede haber otro sitio desde donde pueden ser accedidos. Pero si har que tomar que el acceso es limitado porque es muy probable que el acceso principal sea mediante el hogar; se obervará esto en gráficas subsecuentes.


**Prueba de chi cuadrado**:  
Se hizo la prueba de hipótesis para comprobar que la distrbución de dispositivos no es aleatoria, y que la asociación   
entre variables es significante:

Valor p: 0.0001
Para más referencia revisar el documeto proporcionado.

#### Porqué no se tiene acceso a una computadora en el hogar <a id="7"></a>

Dentro de la encuesta se enlista razones del porque no se tiene una computadora en casa, y esto es lo que se  
respondió en los hogares:

![Razones del porque no se cuenta con una computadora](/Graphs/NoComp_hog.png)

La principal razón es por falta de recursos económicos, seguida por la falta de interés y el no saber usar una computadora. Si bien, se expone presisamente la problemática económica, la cual desde el principio es una razón importante, también se exhiben razones de uso que se alejan un poco del aspecto puramente económico. 
El desinterés o la no necesidad, así como el no saber usarla revela que hay otro tipo de brechas que pueden intervenir dentro de esta falta de acceso.

### Usuarios de TIC's en México <a id="8"></a>

Si tienes interés del proceso de manipulación y gráficado de datos de esta sección, visita el siguiente notebook contenido en este repositorio:

[Notebook de Usuarios de Computadoras y Smartphones](/jupyter_notebooks/2.3.-Tics_user.ipynb)

#### Usuarios de TIC's por Estrato Socioeconómico <a id="9"></a>

El tener acceso en el hogar a cierta tic en la vivienda no significa que los miembros de los hogares sean usuarios de la misma, así como ese acceso no restringe a la persona a ser usuaria, pues se puede considerar como tal aunque no se tenga acceso desde el hogar.

![Usuarios de tics](/Graphs/Tics_usu_sci.png)

Está gráfica representa lo que se dijo al principio. La cantidad de usuarios de Smartphones tiende a permanecer equivalente, y hay algo que notar con los usuarios de internet, pues estos no solo no disminuyenm sino que aumentan y se equiparan a los usuarios de los Smartphones, aunque en el hogar según el estrato no haya acceso a esta Tecnología. Se puede pensar que el acceso a Internet puede suceder en otros lugares, y así se verá. 

Respecto a los usuarios de Computadoras, estos disminuyen por Estrato Socioecconómico, respecto al acceso en los hogares como con las otras tic, Smartphone e Internet:
- Usuarios de Computadora del Estrato socioeconómico Alto: 66.79%
  - Acceso Computadora en el hogar: 76.43%
- Usuarios de Computadora del Estrato socioeconómico Medio Alto: 49.06%
  - Acceso Computadora en el hogar: 57.67%
- Usuarios de Computadora del Estrato socioeconómico Medio Bajo: 31.25%
  - Acceso Computadora en el hogar: 36.25%
- Usuarios de Computadora del Estrato socioeconómico Bajo: 11.61%
  - Acceso Computadora en el hogar: 13.49%

#### Desde que lugar acceden más a internet los usuarios <a id="10"></a>

![Acceso a computadora general](/Graphs/Acceso_compgen.png)


