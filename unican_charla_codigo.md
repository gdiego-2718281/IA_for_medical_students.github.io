2026-10-12

```table-of-contents
title: 
style: nestedList # TOC style (nestedList|nestedOrderedList|inlineFirstLevel)
minLevel: 0 # Include headings from the specified level
maxLevel: 0 # Include headings up to the specified level
include: 
exclude: 
includeLinks: true # Make headings clickable
hideWhenEmpty: false # Hide TOC if no headings are found
debugInConsole: false # Print debug info in Obsidian console
```



---
title: "Inteligencia Artificial"
subtitle: "para estudiantes de medicina"
author: "fjgdiego"
institute: "CS Astillero"
date: "última actualización (updated: `r Sys.Date()`)"
output:
  xaringan::moon_reader:
    css: [default,metropolis-fonts,"assets/my-style.css"]
    lib_dir: libs
    self_contained: true
    nature:
      ratio: "16:9"
      highlightStyle: github
      highlightLines: true
      countIncrementalSlides: false
      countdown: 45000
      
---
class: inverse

```{r setup, include=FALSE}
options(htmltools.dir.version = FALSE)

library(fontawesome)
        
```

```{css, echo = FALSE}
.letra-chica {
  font-size: 70%;
}
.letra-mediana {
  font-size: 18px;
}

```

```{r xaringanExtra, echo=FALSE}
library(xaringanExtra)

xaringanExtra::use_banner(
  bottom_left = "fjgonzalez-diego",
  exclude = "title-slide"
)


```


# De qué no vamos a hablar

.pull-left[

<img src ="img/fallout.png">

]

.pull-right[

<img src ="img/BG1.webp">

]


???



---

background-image: url("img/newton.webp")
background-position: 95% 5%
background-size: 100px
background-color: #FCE300

# En un lugar de la Mancha...

.pull-left[
Unos 300 años atrás...un grupo de filósofos y matemáticos creaban el entramado de la ciencia moderna:
<center>.content-box-red[observación | experimentación | herramientos matemáticas]</center>

no sólo estaban interesados en el universo físico, sino también en el estudio de la mente, con las mismas herramientas matemáticas

`r fontawesome::fa("user")` **Thomas Hobbes** .letra-chica[razonamiento como un sistema de cálculo]
`r fontawesome::fa("user")` **René Descartes** .letra-chica[números asignados a pensamientos]
`r fontawesome::fa("user")` **Gottfried Wilhelm Leibniz** .letra-chica[aritmética para describir el razonamiento humano]

`r fontawesome::fa("user")` **George Boole**, .letra-chica[a mediados s.XIX solucionó el problema que Leibniz no pudo, con una nueva forma de álgebra &rarr; desarrollo de la lógica formal y ordenadores.]


]

.pull-right[

Mediados s.XX con la **Revolución Cognitiva** surgió el campo de la ciencia cognitiva.

Hay límites en la lógica formal, se desarrollaron nuevos enfoques matemáticos: 
- **ANN** (sistemas matemáticos que imitan el funcionamiento del cerebro)
- **modelos Bayesianos** (cómo capturar el conocimiento previo y tratar con la incertidumbre)

<img src ="img/en-un-lugar.png">

]


---
class: inverse
background-color: #0148A4

# De qué vamos a hablar?

```{r eval=FALSE, tidy=FALSE, echo = FALSE}
remotes::install_github("yihui/xaringan")
```

.pull-left[
<img src ="img/one-million.jpeg" height=400px>

]

.pull-right[

<img src="img/nivel-10.jpeg" height=320px>

]

---
class: middle, center, inverse
background-color: #0148A4

# Definición IA

.left-column[
<img src ="img/EU_AI_Act.png"/>

]

.right-column[

.pull-left[

.red[<h4>sistema de IA</h4>]

 un sistema basado en máquinas

 que está diseñado para funcionar con diversos
niveles de autonomía y 

 que puede mostrar capacidad de adaptación tras su despliegue, y que, 

 para objetivos explícitos o implícitos, infiere, a partir de la entrada que recibe, 

 cómo generar salidas tales como
predicciones, contenidos, recomendaciones o 
decisiones 

 que pueden influir en entornos físicos o 
virtuales
]

.pull-right[

<img src ="img/ramas_IA.png"/>

]



]

---
class: middle, center, inverse
background-color: #1B9BBB

# Tipos de AI: contexto temporal

<div style="position: absolute; top: 50%; left: 5%; transform: translateY(-50%);">
<img src ="img/contexto_historico_bis.png" width=550px/>
</div>




.pull-right[
<img src ="img/contexto_historico_diagram.png" height=475px/>
]


---

background-image: url("img/story-of-my-life.png")
background-size: contain

---
class: center
background-image: url("img/timeline-revolution.webp")
background-size: contain

# La cuarta revolución industrial

---
class: inverse
background-color: #E64626

# Qué sabemos?

<center>Encuesta Medscape-Univadis en primer cuatrimestre de 2024, 1003 médicos en activo (60% hombres, 94% mayores 40 años, 19% AP, 7% MI, 64% otras especialidades)</center>

.pull-left[

<img src ="img/univadis-grado-conocimiento-medicos.png" width=400px height=200px>

<img src ="img/univadis-importancia.png" height=200px>

]

.pull-right[

.pull-left[<img src ="img/univadis-uso.png" width=350px height=400px>]

.pull-right[<img src ="img/univadis-opinion-futuro-IA.png" height=200px>]

]

---
class: inverse
background-color: #E64626

# Y la población? `r fontawesome::fa("users-gear", fill = "blue")`

.pull-left[

#### Consumo diario de información a través de distintos canales 

<img src = "img/canales_comunicacion.png" />

<h6>https://www.fecyt.es/sites/default/files/2026-07/001_Maqueta-IBERIFIER-Reports-Desinformacion-cientifica-en-Espana_fecyt-ACCESIBLE.pdf</h6>
]

.pull-right[



<img src = "img/fecyt_confianza.png" />

]




???
Una encuesta* sobre desinformación científica en España difundida por la Fundación Española para la Ciencia y la Tecnología (Fecyt) arroja luz sobre el consumo de información científica, la percepción sobre la recepción de bulos o el auge del uso de la inteligencia artificial para consultar asuntos sobre salud, entre otros aspectos.

*2.215 mayores de 16 años encuestados con preguntas de respuesta múltiple. Las categorías no eran excluyentes, por lo que los porcentajes no suman 100%.

---
background-image: url("img/gr2.png")
background-size: cover




---
class:inverse
background-color:#1B9BBB


# La historia de la IA se puede resumir en 3 etapas



.pull-left[

Three major eras in AI development:

- .content-box-army[1950s-1970s]: Foundational development with rule-based systems like MYCIN and Eliza chatbot

- .content-box-army[1970s-2000s]: "AI winter" period with limited funding, followed by renewed interest with expert systems

- .content-box-army[2000s-2020]: Explosive growth with deep learning, natural language processing, and cloud-based applications

]




.pull-right[

- 1940-1970 entender la lógica del razonamiento del médico en la máquina
  - el optimismo inicial se topó con la cruda realidad de la complejidad médica
  - codificar manualmente todo el conocimiento médico era inviable
  
- invierno de la IA por las limitaciones computacionales

- le dejamos de dar a la máquina las reglas y le dimos los ejemplos, para que los encontrara directamente, aunque el potencial era limitado por cuestiones técnicas
]


---
background-image: url("https://cyberneticzoo.com/wp-content/uploads/neuron-SNARC-GJLoan2011-x640.jpg")
background-position: 95% 15%
background-size: 200px

# Era teórica y fundacional (1940-1960)



**Qué era la inteligencia**`r fa("question", fill = "blue", height = "2em")`

.pull-left[

- 1943 - primer modelo matemático de una neurona (neurocientífico Warren McCullogh y el lógico Walter Pitts)
  - idea revolucionaria: unidades muy simples pueden computar cualquier función lógica

- .content-box-red[1950 - Turing] (pueden pensar las máquinas?)
  - <b>juego de la imitación</b>


.right[<img src="img/WarrenMcCulloch-WalterPitts.png" height=160px/>]
]
  
.pull-right[

- 1951 - primera máquina de red neuronal (Marvin Misnky/Dean Edmonds) que simulaba una rata encontrando el camino por un laberinto
  - <b>Snarc</b> Stochastic Neural Analog Reinforcement Computer 

- .content-box-red[1956 - conferencia de Dartmouth] &rarr; se acuña el término de <b>Inteligencia Artificial</b>

- 1957 - avance definitivo <b>Perceptron</b> de Frank Rosenblat, aprendía a reconocer patrones

.left[<img src="img/alan-turing-1.webp" width=200px/>]

]


???
el SNARC era un dispositivo analógico formado por 40 tubos de vacío, resistencias y condensadores, ensamblados para representar nodos y conexiones similares a las neuronas del cerebro humano. Su objetivo no era realizar cálculos a gran velocidad, sino imitar el modo en que los organismos aprenden a partir de la experiencia.
1951 – SNARC Maze Solver – Minsky / Edmonds (American)

In 1951 Marvin Minsky teamed with Dean Edmonds build the first artificial neural network that simulated a rat finding its way through a maze.

They designed the first (40 neuron) neurocomputer, SNARC (Stochastic Neural Analog Reinforcement Computer), with synapses that adjusted their weights (measures of synaptic permeabilities) according to the success of performing a specified task (Hebbian learning) The machine was built of tubes, motors, and clutches, and it successfully modeled the behavior of a rat in a maze searching for food.

As a student, Minsky had dreamed of producing machines which could learn by providing them with memory "neurones" connected to "synapses"; the machine would also have to possess past memory in order to function efficiently when faced with different situations.

In 1951 the "machine" was born, consisting of a labyrinth of valves, small motors, gears and wires linking up the various "neurones". Some of these wires were connected up at random to the various memory banks in order to achieve a degree of causality of events. The reason such a machine had been put together was to try and find the exit from a maze where the machine would play the part of a rat whose progress would be monitored on a light network.

When the system was completed it was possible to follow all the movements of the 'rat' within the maze and it was only through a design fault that it was found more than one 'rat' could be introduced which would then interact together. After various casual attempts the rats started 'thinking' on a logical basis helped along by reinforcement of correct choices made and the more advanced rats would then be followed by the ones left behind. This first practical example, built by Minsky with the help of Dean Edmonds, also included numerous casual connections between its various 'neurones', acting like a sort of nervous system able to overcome any eventual information interruption due to one of the neurones failing.


---

# Perceptron

.pull-left[

<img src="img/perceptron_simple.png"/>

]

.pull-right[

<img src="img/perceptron_vs_neuron.png"/>

]

- es un algoritmo para el aprendizaje supervisado de clasificadores binarios.
  
  - Un clasificador binario es una función que puede decidir si una entrada, representada por un vector de números, pertenece o no a una clase específica.

- El modelo biológico más simple de un perceptrón es una neurona y viceversa

---
background-image: url("img/MYCIN.webp")
background-position: 95% 5%
background-size: 200px

# Primeros sistemas expertos<br/>(1970s)

.pull-left[
- DECsystem-10
  - se pasó de decenas de miles de transistores a 1000-50.000 millones
![:scale 70%](img/decsystem-10.jpg)

- **INTERNIST-1**, era más complejo

]

.pull-right[

.pull-left[

**MYCIN**, sistema de diagnóstico y tratamiento de infecciones bacterianas


![:scale 75%](img/MYCIN.jpg)
]

.pull-right[

**CASNET**, en glaucoma (tenía en cuenta las causas, no sólo los síntomas, razonamiento basado en modelos)


![:scale 75%](img/CASNET3layer.gif)
]


]


???

En los 1970s primeros sistemas expertos, su objetivo era capturar el conocimiento de un experto humano que se ejecutaba en un ordenador como el que se ve.
Usaba decenas de miles de transistores.
  - un procesador actual va desde más de 1000 millones hasta 50.000 millones de transistores
  
El sistema más icónico del momento fué MYCIN desarrollado en Stanford para el diagnóstico y tratamiento de las infecciones bacterianas
  - usaba 600 reglas del tipo if...then
  - manejaba la incertidumbre con valores de certeza, asignaba un grado de confianza a cada conclusión en vez de usar probabilidades estrictas, imitando el razonamiento clínico
  - su rendimiento llegó a ser comparable al de los médicos expertos, pero nunca se usó en la práctica: ordenadores lentos y de enormes dimensiones y requerían que un médico introdujera manualmente decenas de datos lo que hacía inviable su uso en la práctica clínica
  
Otro sistema fué INTERNIST-1 que intentó abarcar toda la medicina interna, un objetivo mucho más ambicioso, y esta complejidad fué su talón de aquiles, ya que tenía dificultad para manejar casos con múltiples patologías simultáneas.

Luego estaba CASNET, aplicado exclusivamente al glaucoma
  - intentó algo diferente, no se limitó solo a los síntomas sino que modeló las causas de la enfermedad, fué un enfoque más profundo conocido como razonamiento basdo en modelos, que buscaba entender el porqué fisiopatológico, no solo el diagnóstico puro
  
A pesar de estos avances, a principios de los80s, llegó la gran decepción.
  




---
class: inverse
background-image: url("img/AI_winters.jpg")
background-position: 95% 5%
background-size: 250px

# Primer invierno de la IA (1980s)

**Principales cuellos de botella** `r fa("wine-bottle", height = "2em")` 

- **Ingeniería del conocimiento**
  - extracción y codificación del conocimiento médico, para ser usado por los sitemas expertos
  
  - conocimiento tácito de expertos &rarr; reglas explícitas, 
    - un médico experto no usa un *si...entonces*
    - usa la experiencia, la intuición y un contexto que no es posible programar

- limitado poder computacional de la época (lentos, caros y requerían de personal altamente especializado)

- falta de resultados tangibles

Hubo una crisis de confianza.

--

Segundo invierno a principios de los 90s, por ineficiencia de las NN.

???
A principios de los 1980s la gran decepción.

La extracción y codificación del conocimiento implicaba largas entrevistas con expertos, para intentar convertir su conocimiento tácito, a menudo intuitivo, en reglas lógicas y explícitas.

La evidente falta de resultados tangibles que justificaran la enorme inversión.
Los gobiernos e inversores, que habían sido seducidos con la promesa de máquinas inteligentes, se sintieron defraudados.

Culminó en el primer invierno de la IA, donde el interés y la financiación se desplomaron drásticamente: los proyectos se cancelaron, los laboratorios se cerraron, y el término de IA se convirtió en un tabú, dejando el campo en un estado de hibernación, a la espera de un nuevo enfoque.

---
class: inverse
background-image: url("img/AI_winters.jpg")
background-position: 95% 5%
background-size: 250px

# Tras un segundo invierno<br/> (inicios 1990s)

.pull-left[

- entrenar estas redes era lento

- sobre todo por el **desvanecimiento del gradiente**, las capas más profundas no aprendían correctamente, impidiendo que ella misma siga aprendiendo

![:scale 40%](img/segundo_invierno.png)
]

.pull-right[

- se cambió el foco hacia aprendizajes más pragmáticos &rarr; **Aprendizaje Automático (ML)**

![:scale 60%](img/hacia_ML.png)

  - de sistemas basados en reglas &rarr; Aprendizaje donde los algoritmos aprenden patrones directamente de los datos, con métodos más robustos (SVM o árboles de decisión)
  


]

.center[.content-box-army[En segundo plano se construyó la infraestructura hacia el aprendizaje profundo (DL)]]

???
Tras un 2º invierno a principios de los 90s por la ineficiencia de las primeras reedes neuronales, los investigadores se dieron cuenta que entrenar estas redes era lento, sufrían problemas técnicos, como el llamado problema del desvanecimiento del gradiente que impedia que las capas más profundas de la RN aprendieran correctamente, impidiendo que ella misma siguiera aprendiendo después.

---

background-image: url("img/hacia_ML.png")
background-position: 95% 5%
background-size: 200px

# Transición hacia el aprendizaje automático, ML (1990s-2012)

.pull-left[

Dos factores fueron clave en esta época de transición:

- cumplimiento de la .content-box-yellow[Ley de Moore] &rarr; ordenadores más rápidos
  
- digitalización masiva de documentos, de archivos en papel a repositorios digitales inmensos y sistemas PACS, para la imagen médica (resolvió el cuello de botella del conocimiento `r fa("wine-bottle", height = "2em")`)

<br/><br/>
<center><b>Datos &rarr; combustible de los nuevos modelos de aprendizaje</b></center>


.footnote.letra-chica[PACS = Sistema de Archivo y Comunicación de Imágenes]

]

.pull-right[

<img src ="img/Moore_law.png" width = 500px>

]


???

Dos factores fueron clave en esta época de transición:
- el cumplimiento de la Ley de Moore, la predicción de Gordon Moore de que el nº de transistores en un circuito integrado se duplicaría cada 2 años se cumplió rigurosamente, lo que garantizó un crecimiento exponencial y predecible de la potencia computacional, haciendo que cada vez los ordenadores fueran más rápidos y capaces de realizar cálculos más complejos, que serían esenciales para los algoritmos futuros que ya se iban teorizando

- la digitalización masiva de documentos, como la Hª clínica, y la popularización de los sistemas PACS, para la imagen médica, este fué el cambio más decisivo
  - los datos ya no tenían que ser extraidos manualmente en tediosas entrevistas o transcripciones, estaban ahí, accesibles en millones de casos clínicos digitalizados, listos para ser utilizados como el combustibles de los nuevos modelos de aprendizaje.

Como resultado la comunidad científica cambió el foco hacia algoritmos más pragmáticos, basados en el aprendizaje automático. 

La Ley de Moore, formulada en 1965 por Gordon E. Moore, cofundador de Intel, ha sido uno de los principios más influyentes en la evolución de la industria tecnológica. En su esencia, esta ley predice que el número de transistores en un microprocesador se duplica aproximadamente cada dos años, lo que implica un aumento significativo en la capacidad de procesamiento y una disminución del costo por transistor. Aunque originalmente se presentó como una simple observación, la Ley de Moore ha guiado el desarrollo de la tecnología durante más de medio siglo.

El origen de la Ley de Moore
Gordon Moore publicó su predicción en un artículo titulado Cramming More Components onto Integrated Circuits en la revista Electronics. Su análisis se basaba en el crecimiento exponencial que ya se observaba en la integración de transistores en circuitos integrados. En aquel momento, los microprocesadores contenían pocos cientos de transistores, pero Moore vislumbró un futuro en el que esta cifra se multiplicaría de manera exponencial, revolucionando la tecnología.

Aunque Moore predijo inicialmente que esta tendencia continuaría durante una década, la industria tecnológica superó esas expectativas, manteniendo la validez de su observación durante más de 50 años.

La Ley de Moore: el principio que ha definido la evolución de la tecnología 

Impacto en la industria de los semiconductores
La Ley de Moore se convirtió en una hoja de ruta para la industria de los semiconductores, impulsando la innovación y la inversión en la miniaturización de componentes electrónicos. Este fenómeno permitió avances en varios campos:

Aumento en la capacidad de procesamiento: Los microprocesadores más potentes se tradujeron en mejoras significativas en dispositivos como ordenadores personales, teléfonos móviles y supercomputadoras.
Reducción de costos: La miniaturización permitió fabricar componentes más económicos, democratizando el acceso a la tecnología.
Evolución de dispositivos móviles: Gracias a la Ley de Moore, dispositivos como smartphones y tablets pudieron integrar funcionalidades avanzadas en diseños compactos.
Desarrollo de la inteligencia artificial (IA): El incremento en la capacidad de procesamiento fue clave para entrenar modelos de IA cada vez más complejos y eficientes.
Desafíos actuales: ¿el fin de la Ley de Moore?
En las últimas décadas, cumplir con la Ley de Moore se ha vuelto cada vez más desafiante debido a limitaciones físicas y económicas. La miniaturización de transistores ha alcanzado niveles tan pequeños que surgen problemas de disipación de calor, interferencia cuántica y costos de producción extremadamente altos.

La industria ha respondido a estos retos con estrategias como:

Materiales avanzados: Uso de silicio-germanio, grafeno y otros compuestos para mejorar la conductividad y la eficiencia.
Arquitecturas tridimensionales: La fabricación de chips 3D apila capas de transistores, aumentando la densidad sin reducir el tamaño de cada componente.
Procesadores heterogéneos: Integración de diferentes tipos de núcleos en un mismo chip para optimizar el rendimiento y la eficiencia energética.
Aunque algunos expertos predicen el fin de la Ley de Moore en términos estrictamente físicos, otros argumentan que la innovación en diseño y materiales permitirá que su espíritu se mantenga vigente.

Más allá de la Ley de Moore: nuevas fronteras tecnológicas
Ante las limitaciones de la Ley de Moore, la industria se ha volcado en explorar alternativas para mantener el ritmo de progreso tecnológico. Algunos de los enfoques incluyen:

Computación cuántica: Promete superar los límites de la computación tradicional al aprovechar los principios de la mecánica cuántica para realizar cálculos a velocidades inalcanzables para los ordenadores actuales.
Arquitecturas neuronales: Inspiradas en el funcionamiento del cerebro humano, estas arquitecturas buscan optimizar el procesamiento de tareas específicas, como el reconocimiento de patrones y el aprendizaje automático.
Inteligencia artificial especializada: Chips diseñados específicamente para tareas de IA están revolucionando campos como la robótica, la visión artificial y los asistentes virtuales.
Computación basada en ADN: Aunque todavía en fase experimental, esta tecnología utiliza moléculas de ADN para almacenar y procesar información.
El legado de la Ley de Moore
Independientemente de sus limitaciones actuales, la Ley de Moore ha dejado una marca indeleble en la tecnología y la economía global. Su impacto no se limita a la ingeniería de semiconductores, sino que ha influido en la forma en que las empresas planifican el desarrollo de productos y servicios. Ha sido una fuerza impulsora detrás de la innovación tecnológica, permitiendo que la sociedad avance hacia un futuro cada vez más conectado y automatizado.

En última instancia, la Ley de Moore no solo representa una observación científica, sino también un paradigma de ambición y progreso que ha inspirado a generaciones de ingenieros y científicos a superar los límites de lo posible. Su legado continuará siendo un faro para la innovación en los años venideros.

---

background-color: #F08080
# Finales de los 2000s

.center[Más datos, más capacidad de computación.<br/> .content-box-yellow[MYCIN (1972) &rarr; CAD(2006)]]

.pull-left[

.center[<img src = "img/MYCIN.webp" width = 200px>]

<img src = "img/MYCIN_expert_system.png" width = 275px>

]


.pull-right[

<img src = "img/CAD_edad-osea.jpg" width = 290px>

]


.footnote.letra-chica[CAD = Diagnóstico Asistido por Ordenador]


???

En este momento con más datos y mejor computación vieron la luz los primeros sitemas de diagnóstico asistido por ordenador (CAD), su función inicial era simple: actuar como una segunda opinión en el ámbito del diagnóstico por imagen sobre todo (mamografía o rx torax), aunque a menudo sufrían de una alta tasa de FP fueron un paso fundamental para integrar la computación en el flujo de trabajo diagnóstico


CAD is fundamentally based on highly complex pattern recognition. X-ray or other types of images are scanned for suspicious structures. Normally a few thousand images are required to optimize the algorithm. Digital image data are copied to a CAD server in a DICOM-format and are prepared and analyzed in several steps.

---

## Radiómica (2010)

Las imágenes médicas contienen información mucho más allá de lo que el ojo humano puede percibir.

Extracción de cientos/miles de características de la imagen, para construir modelos predictivos (sobre todo oncología).

<b>Su objetivo es</b>
  - convertir las imágenes médicas en datos explotables
  - para lograr resultados reproducibles
  - que contribuyan a mejorar el diagnóstico, pronóstico, estratificación de los pacientes, predicción de respuesta al tratamiento...
  
<center><img src = "img/radiomica.png" height=170px/></center>

<center>.content-box-green[adquisición de imagen&rarr;segmentación (ROI)&rarr;descriptores matemáticos (forma, intensidad pixeles, textura)&rarr;análisis de datos (modelos de IA)]<br/>.letra-chica[<cite>tomada de Gillies et al, 2016</cite>]</center>

???

ROI = región de interés

---

class: inverse
background-image: url("img/gpu.jpg")
background-position: 90% 25%
background-size: 200px
background-color: #F08080

# La era del aprendizaje profundo, DL (2012-presente)

Combinación de tres factores

.pull-left[

- el algoritmo de retropropagación (**backpropagation**)
    - desvanecimiento del gradiente
    
  ![:scale 75%](img/backpropagation-in-Neural-Network.webp)
  ]
  
.pull-right[
  
- GPUs - unidades de procesamiento gráfico

- datos masivos - IMAGENET
  
  ![:scale 85%](img/imagenet.webp)

]

--

AlexNet (2012 &rarr; disminuyó la tasa de error a más de la mitad, respecto al segundo

???

Con este avance llegamos a la era actual, con un crecimiento exponencial gracias a la confluencia de 3 factores que llegaron a su madurez simultánemaente:
1º el algoritmo de retropropagación, aunque conceptualizado décadas antes, por fin pudo ser implementado de forma eficiente para entrenar redes neuronales con muchas capas, minimizando problemas como el desvanecimiento del gradiente
2º GPUs originalmente diseñadas para renderizar gráficos en videojuegos, eran extraordinariamente eficientes para los cálculos matriciales masivos que requieren las RNs, esto proporcionó la fuerza bruta computacional que se necesitaba
3º accesibilidad a datos masivos y etiquetados, como la BD Imagenet, enorme BD visual con millones de imágenes etiquetadas, diseñadas para la investigación en reconocimiento de objetos visuales, su desafio anual se convirtió en la referencia para evaluar el rendimiento de algoritmos de visión por ordenador.

Y aquí viene el punto de inflexión

---

background-image: url("img/alexnet.webp")
background-position: 95% 5%
background-size: 400px

# AlexNet

<br/><br/>

<img src="img/AlexNet_1.png"/>



---
class: inverse
background-color: #1B9BBB
background-image: url("img/fool_data.png")
background-position: 95% 5%
background-size: 150px


# Datos

.pull-left[

<img src = "img/datos.jpg" height=400px>


.footnote.letra-chica[<cite>Una mirada a la era de los datos. Dunstan & Maass & Tobar. Saberes, 2022.</cite>]

]

.pull-right[

<img src = "img/ML_BigData.PNG">

.footnote.letra-chica[Big Data and Machine Learning in Health Care. Beam & Kohane.JAMA, 2018]

]



???

Traditional clinical studies analyze data from hundreds or thousands of patients using a carefully designed statistical model and thus are low on the machine learning spectrum. Deep learning models are at the top of the spectrum. 
At the very top are generative adversarial networks, which can learn to generate new images by examining a large database of existing images


---

# Modelo de aprendizaje automático

<img src = "img/modelo_aprendizaje_automatico.jpg">

???

Modelo de aprendizaje automático 

Este modelo representa la relación entre la entrada (edad del niño) y la salida (altura del niño). El modelo se entrena utilizando datos con relaciones específicas, que consisten en pares de entrada-salida (puntos naranjas). Cuando entrenamos el modelo, describimos pares de datos buscando posibles relaciones. Aquí, las relaciones del modelo entrenado están representadas por curvas cian, que pueden usarse para calcular la altura a cualquier edad.

Más precisamente, el modelo describe un sistema de ecuaciones que asigna entradas a salidas, que coinciden con datos de entrenamiento (datos de entrenamiento) que consisten en pares de entrada-salida. En la Figura 1.3, estos pares de entrada-salida están representados por puntos naranjas y podemos ver que el modelo describe razonablemente estos datos. Cuando hablamos de entrenamiento (entrenamiento) o ajuste (ajuste) de un modelo, en realidad estamos hablando de buscar ecuaciones relacionadas con la entrada y la salida a través de estas posibles ecuaciones para encontrar la ecuación que mejor describa los datos de entrenamiento.


---
background-color: #FCE300

# Cómo se construye un modelo de ML?

.pull-left[

`r fontawesome::fa("screwdriver-wrench", height = "2em")`**Ej.: herramientas que se pueden usar en ML**

<img src ="img/ml101-6-step-ml-framework-tools.png">

<center><img src ="img/ml101-different-data-types.png" height = 110px></center>

]

<div style="display: flex; justify-content: flex-end;">

<img src = "img/building_ML.jpg" height = 450px alt="Cómo construir un modelo de ML, entrenarlo y evaluarlo">

</div>

???

https://github.com/mrdbourke/zero-to-mastery-ml/blob/master/section-1-getting-ready-for-machine-learning/a-6-step-framework-for-approaching-machine-learning-projects.md

Machine learning projects can be broken into three steps, data collection, data modelling and deployment. This article focuses on steps within the data modelling phase and assumes you already have data. Full version on Whimsical.
Problem definition—What business problem are we trying to solve? How can it be phrased as a machine learning problem?
Data—If machine learning is getting insights out of data, what data we have? How does it match the problem definition? Is our data structured or unstructured? Static or streaming?
Evaluation—What defines success? Is a 95% accurate machine learning model good enough?
Features—What parts of our data are we going to use for our model? How can what we already know influence this?
Modelling—Which model should you choose? How can you improve it? How do you compare it with other models?
Experimentation—What else could we try? Does our deployed model do as we expected? How do the other steps change based on what we’ve found?

---

# DL aprendizaje supervisado

<img src = "img/DL_supervisado.jpg" height = 475px width = 600px>

???
Problema de regresión y clasificación 

a) Este modelo de regresión utiliza un vector numérico para representar la propiedad y predice su precio. 

b) Este modelo de regresión múltiple utiliza la estructura molecular de la materia orgánica para predecir sus puntos de fusión y ebullición. 

c) Este modelo de clasificación binaria utiliza reseñas de restaurantes y las clasifica como reseñas positivas o negativas. 

d) Este problema de clasificación múltiple clasifica el audio en uno de varios géneros. 

e) Este es otro problema de clasificación múltiple que clasifica la imagen de entrada en una de varias categorías posibles.]

---
exclude: true

# ejemplo de herramientas que se pueden usar en ML

<img src ="img/ml101-6-step-ml-framework-tools.png">

???

https://github.com/mrdbourke/zero-to-mastery-ml/blob/master/section-1-getting-ready-for-machine-learning/a-6-step-framework-for-approaching-machine-learning-projects.md

Machine learning projects can be broken into three steps, data collection, data modelling and deployment. This article focuses on steps within the data modelling phase and assumes you already have data. Full version on Whimsical.
Problem definition—What business problem are we trying to solve? How can it be phrased as a machine learning problem?
Data—If machine learning is getting insights out of data, what data we have? How does it match the problem definition? Is our data structured or unstructured? Static or streaming?
Evaluation—What defines success? Is a 95% accurate machine learning model good enough?
Features—What parts of our data are we going to use for our model? How can what we already know influence this?
Modelling—Which model should you choose? How can you improve it? How do you compare it with other models?
Experimentation—What else could we try? Does our deployed model do as we expected? How do the other steps change based on what we’ve found?



---
class: inverse
background-image: url("img/U-Net_layered_architecture.webp")
background-position: 95% 5%
background-size: 300px
background-color:#E64626

# Primeras aplicaciones del DL

.center[### U-Net (2015)]

![:scale 80%](img/U-Net.webp)

???

Las CNN (igual que AlexNet) se han convertido en el estándar para el análisis de imágenes.
Ya igualan, o superan en ocasiones, a los expertos humanos en tareas de clasificación, como detectar cancer de piel a partir de fotografias o detectar la retinopatia diabética en imágenes de fondo de ojo.

En el campo de la segmentación de imágenes, la arquitectura U-Net de 2015 revolucionó la forma de delinear órganos y tumores, su genialidad reside en su característico diseño en forma de U:
  - una parte de la red, el codificador, reduce la imagen para capturar el contexto general
  - mientras que la otra parte o decodificador, reconstruye la imagen combinando la información de contexto con detalles finos de las capas iniciales, esto le permite combinar la información de distintos niveles de detalle


---
class: inverse
background-color:#E64626

# Primeras aplicaciones del DL (cont...)

<center><b>Cancer de piel clasificado por un algoritmo de DL y por dermatólogos.</b></center>

.pull-left[

<img src ="img/skin_cancer_nihms-1724608-f0001.jpg" height = 200px/>
<img src ="img/skin_cancer_nihms-1724608-f0002.jpg" height = 200px/>
]

.pull-right[
<img src ="img/skin_cancer_nihms-1724608-f0003.jpg" height = 400px/>
]

.letra-chica[Para cada clasificación el algoritmo funcionaba tan bien o mejor que el grupo de 20 dermatólogos.Dataset 129.450 lesiones de piel, se dividió en 127.463 imágenes de entrenamiento y validación y 1942 imágenes con diagnóstico por biopsia; 2032 enfermedades diferentes; la red CNN se entrenó con 757 clases.]

???
Our classification technique is a deep CNN. Data flow is from left to right: an image of a skin lesion (for example, melanoma) is sequentially warped into a probability distribution over clinical classes of skin disease using Google Inception v3 CNN architecture pretrained on the ImageNet dataset (1.28 million images over 1,000 generic object classes) and fine-tuned on our own dataset of 129,450 skin lesions comprising 2,032 different diseases. The 757 training classes are defined using a novel taxonomy of skin disease and a partitioning algorithm that maps diseases into training classes (for example, acrolentiginous melanoma, amelanotic melanoma, lentigo melanoma). Inference classes are more general and are composed of one or more training classes (for example, malignant melanocytic lesions—the class of melanomas). The probability of an inference class is calculated by summing the probabilities of the training classes according to taxonomy structure

---
class: inverse
background-color: #002b49

# Medicina de patrones

<img src ="img/patterns.png">




---



Retinopatía diabetica

---



???

Stephen Weng, 2017
Can machine learning impro cardiovascular risk prediction using routine clinical data?

---


???

Universidad de Stanford, Pranav Rajpurkar, 2018
112.120 radiografías
14 posibles patologías

---

Arquitectura U-Net (2015)

<!-- incluir img -->

---

GANs (2014)

---

Radiómica potenciada por el DL


---

### U-Net (2015)

---

### Redes Generativas Antagónicas (GANs)

---

### Radiómica (2010)

---

### PNL (Procesamiento del Lenguaje Natural)


.pull-left[

Hay arquitecturas novedosas, el gran avance son los <b>Transformers</b>

<img src = "img/transformer_explicado.png" height = 250px/>

Su innovación clave es el <b>mecanismo de atención</b>: permite sopesar las diferentes palabras en un texto capturando contexto y relaciones a distancia

Esto ha llevado al desarrollo de los <b>modelos fundacionales</b> (ej.: los GPTs)
]

.pull-right[

Lo más relevante, aunque están pre-entrenados con gran cantidad de datos de internet, pueden ser perfeccionados con facilidad, mediante <b>fine-tunning</b> (ajuste fino).

<img src = "img/LLM_fine-tunning.png"/>
]


---

D:/OBSIDIAN_notes_2/charla_IA_unican/img/VID_20260908_090055_447.mp4

---

background-color:#FCE300

# Como resumen

.pull-left[
`r fa("ruler-horizontal", height = "2em")`Hemos pasado de la lógica de un médico con reglas fijas &rarr; sistemas que aprenden <b>patrones complejos</b> a partir de cantidades ingentes de <b>datos</b>

<img src ="img/conclusion.png" width = 450px height = 350px>

]

.pull-right[


`r fa("wine-bottle", height = "2em")` El progreso ha sido superar cuellos de botella sucesivos<br/>

.content-box-red[razonamiento&rarr;conocimiento&rarr;computación]

`r fontawesome::fa("bullseye", height ="2em")` El desafio actual es .content-box-red[cómo integrar en los flujos actuales de trabajo estas herramientas] de forma
  <center>segura | ética | eficaz</center>
  
<center><img src ="img/ai_evolution.jpg" height = 250px></center>

]



---
class: inverse
background-color: #1B9BBB
background-image: url("img/caja-negra3.png")
background-position: 95% 5%
background-size: 200px



# Incorporación de la IA a la relación médico-paciente
<center><b>Dónde estamos?</b></center>

<i>Informe del Consejo Europeo</i>

.left-column[


<img src="https://www.coe.int/documents/10518249/123746347/AI+cover-EN.png/fe782c32-b123-e6df-70f6-06907031e49b?t=1652783254000" height="350px">
]

.right-column[

.pull-left[

- la IA redistribuye tareas cognitivas: el médico interpreta y valida, IA filtra y prioriza

- sistemas de alta autonomía y soporte terapéutico

- interacción médico-paciente mediada por IA

- riesgo: percepción de la IA como decisor real
]

.pull-right[
<b>Problemas en 6 áreas</b>

<i>
- desigualdad en el acceso
- transparencia (ligado al CI)
- riesgo de sesgos
- dilución de la narrativa del paciente
- sesgo de automatización y deskilling
- privacidad
</i>

]
]
???

---
class: center
background-color: #1B9BBB


.left-column[
<img src = "img/relacion-medico-paciente.png" height="600px">
]
<h2>Algunos términos de la relación médico-paciente explicados</h2>

.letra-chica[
.right-column[

| Término |Definición  | Relevancia |
|:---|:---:|:---:|
|Human-in-the-loop|la IA emite recomendaciones<br/>la decisión final es humana|refuerza responsabilidad médica y la confianza|
|IA autónoma|decisiones diagnósticas/terapéuticas sin intervención humana|reduce el contacto directo<br/>genera dudas de responsabilidad|
|XAI|decisiones de la IA interpretadas y explicadas|facilita la transparencia|
|Fatiga de alertas|exceso de notificaciones<br/>con pérdida de atención|reduce la seguridad y<br/>eficacia de la comunicación|
|Ruido algorítmico|información irrelevante o errónea|aumenta la confusión<br/>dificulta la comunicación|
|Sesgo algorítmico|datos de entrenamiento<br/>que conducen a un error sistemático|genera inequidades<br/>deteriora la confianza|
|Autonomía del paciente|derecho a decidir|explicar el papel de la IA<br/>y opciones|
|Toma de decisiones aumentada|capacidad analítica aumentada por la IA<br/>se mantiene supervisión humana|mejora calidad de la consulta<br/>y percepción de competencia|
|Validación clínica|beneficio y seguridad demostrados<br/>en la práctica real|garantiza evidencia sólida|
]

]

---
class: middle, center
background-color: #424242
background-image: url("img/high-tech-brain.jpg")
background-size: contain


# El cerebro



---
background-color: #FCE300
background-image: url("img/carga-cognitiva-supermercado-te.webp")
background-position: 5% 5%
background-size: 200px

.pull-left[ 

Ley de Miller: 
- solo podemos recordar +/- 7 elementos (George Miller, 1956)
- esta relacionado con la <b>carga cognitiva</b> 
- si se llega al límite &rarr;<b>parálisis por análisis</b>

**El problema Ferrari de la IA**: *el motor ruge a 300km/hr impulsado por algoritmos, el chasis humano se quiebra ante una aceleración para la que nunca fué preparado*

<img src = "img/ferrari.png" height=100px>

- el verdadero cuello de botella - el ancho de banda cognitivo humano
- tu cerebro
  - información visual ~10 millones bits/seg (*el cerebro procesa las imágenes mucho más rápido que las palabras individuales*)
  - información de texto ~100 bits/seg
  


]

.pull-right[
Desigualdad de ancho de banda

<img src = "img/ancho_banda.png" height=100px>



> — 1 millón de bits/seg vs 10 bits/seg<br/>
> — podemos procesar en 13 msg una escena pero leer una palabra podemos tardar 300 msg<br/> [*parpadeo humano 100-400msg*]<br/>
> — ventaja de velocidad visual x 10-20 veces (MIT Research)<br/>
> — memoria de trabajo: retenemos 7&#177;2 items al mismo tiempo (Ley de Miller)

<img src="img/img_words.png" height=150px>



]

???
Ley de Miller
Se basa en los estudios psicológicos realizados por George Miller en 1956, en los que trataba de comprender cómo funciona la memoria inmediata y cuánta capacidad de recordar tenemos. Su conclusión fue que solo podemos recordar +/- 7 elementos sin morir en el intento.

Está relacionada directamente con la carga cognitiva que menciona Steve Krug en “No me hagas pensar”: nuestro cerebro está constantemente tratando de comprender qué hay a su alrededor y cuantas más entradas de información y combinaciones posibles de soluciones tenga delante, más le costará funcionar adecuadamente.

Si se llega al límite de la carga cognitiva es posible que se produzca la llamada parálisis por análisis, que no es más que la incapacidad de tomar una decisión. Esto suele llevar al usuario a abandonar el producto o el proceso en el que estána inmers@.



---

#la regla de los tres segundos


La regla de los tres-segundos: si un humano no puede verificar o qué hacer sobre un resultado de la IA en 3', dejan de usar la herramienta (se trata de la energía mental que necesitas)

Los equipos que solucionen el problema de verificación tendrán ventajas exponenciales sobre aquellos que no.

.pull-right[

## Cómo construir una mejor IA?
...para disminuir la carga cognitiva

- usar representaciones visuales

- ofrecer verificación incremental (dividir en pequeñas tareas)

- preservar el contexto para el usuario

Lo verdaderamente relevante es cómo crear la interfaz gráfica de usuario para la IA

]

---

# Impacto conceptual en la práctica clínica

- herramientas de IA = predictiva/prescriptiva integrada en flujos clínicos

- usos: diagnóstico asistido, personalización terapéutica, seguimiento longitudinal

- IA autónoma vs IA asistida (human-in-the-loop)

- nivel de autonomía define rol y responsabilidad legal


---

# Despliegue actual


.pull-left[

- AI Act y MDR redefinen criterios de seguridad y validación

- despliegue desigual: alta en hospitales de referencia, baja en primaria

- integración como módulo nativo de HCE

- enfoque en IA explicable y auditabilidad


*La clave es generar confianza.*

]

.pull-right[

<img src="img/IA_EU_Act.png">

]




.footnote[MDR = Reglamento de Dispositivos Médicos<br/> AI Act = Ley Europea de Inteligencia Artificial (entró en vigor el 1 agosto 2024)]

---
background-color: #FCE300

# Arquitecturas en uso clínico

- `r fa("robot", height = "2em")` CNN en imagen
  - clasifican y segmentan lesiones con precisión submilimétrica

- `r fa("robot", height = "2em")` Modelos de secuencia (LSTM, GRU)
  - en monitorización y predicción del deterioro

- `r fa("robot", height = "2em")` Transformadores multimodales
  - combinan datos clínicos, imagen y texto

<center>.content-box-grey[Tipo de arquitectura &rarr; condiciona interpretabilidad y potencial de error]</center>



.letra-chica.footnote[LSTM (Long Short-Term Memory) y GRU (Gated Recurrent Unit)]

???

LSTM (Long Short-Term Memory) y GRU (Gated Recurrent Unit) son dos tipos de redes neuronales recurrentes diseñadas para superar las limitaciones de las RNN tradicionales.

Es decir, están diseñadas especialmente para superar el problema del desvanecimiento del gradiente.

Ambas arquitecturas permiten que la red recuerde información importante durante secuencias largas, lo que las hace ideales para:

-Traducción automática
-Generación de texto
-Análisis de sentimientos
-Predicción de series temporales

Tener en cuenta métricas, entrenamiento, validación

---


.pull-left[

### Entrenamiento y validación clínica

- validación externa en población objetivo antes de despliegue

- métricas clínicas adaptadas al uso real, nos solo AUC o precisión técnica

- .content-box-red[riesgo de **dataset-shift**] en traslación entre centros o países

- validación incluye impacto en decisiones y resultados en salud

]

.pull-right[

### Métricas clínicas relevantes

- sensibilidad y especificidad interpretadas según prevalencia en una población y consecuencias

- NNT y NNH aplicados a la IA: traducir predicciones en impacto tangible

- métricas post-implantación para auditoría continua

- .content-box-red[**valor real** = reducción de eventos adversos<br/> + optimización de recursos]

recursos = sobre todo tiempo `r fa("clock")`
]



---

# Interpretabilidad y adopción clínica


.pull-left[
- transparencia = .content-box-red[confianza] &rarr; mayor uso por médicos (monitorizar siempre los resultados)

- .content-box-red[interpretabilidad] traducida a explicaciones médicas accionables

- riesgo: explicaciones erróneas si no reflejan causalidad clínica

- ajustar explicabilidad a criticidad de la decisión

<img src ="img/percepcion-medico-usa-IA.png" width =450px>

]

.pull-right[

<h4>Integración y posición del humano</h4>

- la integración en HCE debe garantizar .content-box-red[control médico final]

- .content-box-red[interfaces] muestran grado de confianza y razonamiento (evitar carga cognitiva)

- el médico confirma, corrige o rechaza recomendación

- protocolos claros de .content-box-red[autoría] para evitar desplazamiento de responsabilidad
]

???

Hay estudio en USA que los pacientes que saben que su médico usa la IA tienen menos confianza en ellos

REis M, Reis F, Kunde W. Public perception of physicians who use artificial intelligence

---
class: inverse
background-color: #1B9BBB

.pull-left[

### Ej.: Oncología: supervisión  y responsabilidad

- la IA propone ajustes según respuesta intermedia

- la validación multidisciplinar evita automatización acrítica

- la historia clínica debe reflejar autoría humana

- comunicación clara al paciente sobre .content-box-army[rol de la IA]
]

.pull-right[

### Ej.: Cardiología: gestión de alertas

- optimizar alerta útil vs ruido para predicción de eventos

- sobrecarga de alarmas reduce atención a señales críticas (deben añadir valor)

- configurar alertas según perfil del paciente

- balance:<br/>prevención eventos no-deseados `r fa("balance-scale", fill = "#2ed573", height ="2em")` carga cognitiva del clínico

]


???

Recordar el fracaso de Watson de IBM, cuando se aplicó a oncología


---
class: inverse
background-color: #1B9BBB

# Monitorización remota: continuidad asistencial

- wearables con IA para seguimiento proactivo

- riesgo: exceso de datos irrelevantes &rarr; sobrecarga médica

- filtrado inteligente con criterios clínicos (aquello que sirve para decisoones críticas)



???

Sobrecarga de señales
Pueden modificar negativamente la relación por el ruido

---

# GDPR y práctica clínico

- principios: minimización, exactitud, limitación de propósito

- derecho a saber si una decisión se basa en IA

- documentar pseudonimización y evaluación de impacto (DPIA)

.letra-chica[GDPR = Reglamento General de Protección de Datos]


---

# MDR: dispositivos médicos


.pull-left[

- software médico como dispositivo: clases IIa, IIb, III

- .content-box-red[evaluación clínica obligatoria antes de comercialización]

- auditorías post-mercado para detectar fallos y sesgos
]



.pull-right[

<center><h4>Clasificación de dispositivos médicos basada en el nivel de riesgo</h4></center>

<img src ="img/infografia_clasificacion_productos_MDR.webp" height=350px>
]

---

# Relación médico-paciente en la era de la IA

- IA como tercer actor en la consulta

- mantener contacto visual y empatía

- explicar decisiones y rol de la IA en lenguaje comprensible

<!-- incluir img como mejorar comunicación -->


--

# Etica y decisión compartida

- .content-box-red[principios bioéticos]: beneficiencia, no-maleficiencia, autonomía, justicia

- evaluación de sesgos y equidad en modelos

- participación activa del paciente en decsiones mediadas por IA


---

# Del presente al futuro

.pull-left[

- inteligencia &harr; soporte físico

- la inteligencia biológica es muy ineficaz

- la comunicación entre humanos es de varios bits /segundo

- ningún humano sabrá nunca tanto como GPT-4 (.letra-chica[<cite>Geoffrey Hinton, Premio Nobel de Física 2024</cite>])

<img src="img/geoffrey-hinton-cientifico-inteligencia-artificial.webp" height=225px>
]

.pull-right[


El futuro de la inteligencia según Hinton


]

---
background-color:#FCE300

# Retos de la implantación en Sanidad

- <h3>Generación</h3>
  - IA como asistente creativo, generando textos, imágenes o informes
  - Ej.: redactar un informe de alta

- <h3>Automatización</h3>
  - integración en flujos clínicos para aceleerar tareas repetitivas
  - Ej.: cribado de imágenes radiológicas

- <h3>Agentificación</h3>
  - IA que toma decisiones y actúa, con supervisión
  - Ej.: ajuste independiente de parámetros de un ventilador mecánico
  
Implicaciones en seguridad, confianza, y roles clínicos.

---

# Modelos de interacción humano-IA según autonomía

- Humano en el centro (Generación)
  - control total por el profesional
  - IA como apoyo puntual
  
- Humano en el bucle (Automatización)
  - la IA opera
  - el humano decide en tiempo real
  
- Humano como supervisor (Agentificación)
  - IA autónoma
  - revisión posterior del humano
  
Implica cambios normativos, culturales y tecnológicos.

---
background-color: #FCE300

# Está la IAG cerca?

.pull-left[

- la experiencia humana integra múltiples sentidos, no solo lenguaje

- las leyes de escalado mejoran el rendimiento, pero no garantizan el razonamiento

- necesidad de modelos del mundo y aprendizaje auto-supervisado

<img src ="img/la-singularidad-esta-cerca.webp" height=200px>

]


.pull-right[

<img src ="img/singularidad-mas-cerca.webp" height=450px>

]

---

# Embodied AI

.pull-left[

- sistema de inteligencia artificial que no se queda encerrado en la nube, sino que  está ligado a un cuerpo o entorno físico con el que interactúa

- en lugar de procesar texto o imágenes:

  - percibe con sensores (cámaras, micrófonos, tacto...)
  
  - actúa con un cuerpo (brazos robóticos, drones, ruedas...)
  
  - aprende de la interacción con el mundo real o virtual, no solo de bases de datos estáticas
]

.pull-right[
<img src = "img/better-than-us.webp">
]

---

# Areas de impacto en Salud

- investigación
  - desde la formulación de hipótesis hasta la metodología y la diseminación de los resultados
  - uso de datos sintéticos para entrenar modelos respetando la privacidad
  - brazos de control sintéticos
  - ensayos clínicos in-silico para acelerar la validación

- formación y entrenamiento

- práctica clínica
  - apoyo en la recogida estructurada de datos
  - ayuda en la toma de decisiones
  - sistemas de navegación quirúrgica
  - personalización de tratamientos

- gestión


---

# Investigación con datos sintéticos


---


# Brazos de control sintéticos


---

# Descubrimiento de nuevos fármacos


---
class: inverse
background-color: #E64626

# Formación: necesidad de competencias

.pull-left[

- alfabetización en datos y fundamentos de IA

- Interpretación crítica de resultados generados por IA

- comprensión de riesgos, sesgos y limitaciones

- conocimiento de requisitos éticos y regulatorios

]

.pull-right[
<img src="img/core_skills_2030.jpg" height=300px>
<img src="img/tus_core_skills.jpg">
]

---

# Transformación de la enseñanza

.pull-left[
- uso de entornos virtuales y simulaciones realistas para la práctica clínica

- aprendizaje adaptativo personalizado según progreso del estudiante

- evaluación continua y retroalimentación instantánea

<img src= "img/surgery2.png" height=200px>

<h6>Bkheet, E., D’Angelo, AL., Goldbraikh, A. _et al._ Using hand pose estimation to automate open surgery training feedback. _Int J CARS_ **18**, 1279–1285 (2023)</h6>


]

.pull-right[

<img src= "img/daVinci.webp" height=450px>

]

---

# Evaluación del aprendizaje

- integración de escenarios asistidos por IA en evaluaciones prácticas

- medición de competencias técnicas y no técnicas

- uso de métricas objetivas para valorar progreso

---
class: inverse
background-color: #1B9BBB

# En clínica a corto plazo (< 5 años)

- mejora de la precisión diagnóstica mediante IA en imagen y datos clínicos

- asistencia en procedimientos quirúrgicos con sistemas robotizados y navegación

- integración en múltiples especialidades médicas

---
class: inverse
background-color: #1B9BBB

# En clínica a medio plazo (~10 años)

- incremento de rendimiento diagnóstico en múltiples áreas, mediante modelos de visión y **modelos fundacionales clínicos**

- requisitos de generalización entre centros, equipos y poblaciones; importancia de la calibración

- asistencia perioperatoria: planificación, guía intraoperatoria y reducción de errores por fatiga/variabilidad

- el rol del clínico se desplaza de ejecutor a **gestor de decisiones asistidas**


---

# Gestión de recursos

.pull-left[
- uso de IA para predecir la demanda y optimizar la asignación de recursos clínicos y materiales
- planificación dinámica de personal y turnos en función de patrones de actividad
- optimización de inventarios y gestión de suministros críticos
- .content-box-purple[automatizaciónde tareas administrativas]: facturación, gestión de citas, verificación de seguros
- procesamiento inteligente de documentos y extracción de información
- reducción de tiempos de tramitación y errores administrativos
- modelos predictivos para identificar áreas de riesgo y oportunidad
- análisis de datos poblacionales para orientar políticas de salud
- herramientas de simulación para planificación a medio y largo plazo


]

.pull-right[

<img src = "img/digital-twin.jpg">

<h6>Digital twin logistics movement control center of South China Hospital of Shenzhen University.<br/>
<i>Sheng wu yi xue Gong Cheng xue za zhi = Journal of Biomedical Engineering = Shengwu Yixue Gongchengxue Zazhi, 01 Apr 2024, 41(2):376-382Language:chi
https://doi.org/10.7507/1001-5515.202310041</i></h6>
]



---
class: inverse
background-color: #E64626

# Dilemas éticos en clínica: autonomía vs IA

- autonomía profesional y riesgo de *overreliance*, necesidad de consentimiento informado cuando proceda

- asignación de responsabilidad (**fabricante-institución-profesional**) y documentación de decisiones

- equidad: mitigación de sesgos y evaluación de poblaciones vulnerables

- .content-box-blue[transparencia y explicabilidad] proporcional al riesgo clínico


---
class: center, middle

# En el entorno sanitario...


.pull-left[
La IA can accelerate tasks, but 

judgment, empathy, and systems thinking are what turn

technology into better outcomes for patients, clinicians, and organizations.

The real advantage will come from leaders who can bridge both worlds.

<img src="img/cerebro-ada.jpg" width=400px>
]

.pull-right[

<img src ="img/sam-altman-chatgpt1.jpg">

<img src ="img/Sam_Altman.png">

]

---

background-image: url("img/humano-robot.jpg")
background-position: 95% 90%
background-size: 300px
background-color: #FCE300

# Las cuatro reglas de la co-inteligencia

1. siempre invite a la IA a la mesa

2. sé el humano en el ciclo

3. trata a la IA como una persona (pero dile qué clase de persona es)

4. asume que esta es la peor IA que usarás


.footnote[Ethan Mollick. Co-Intelligence. Living and Working with AI.]

---
class:inverse
background-image: url("img/replies.png")
background-size:contain

---

FINISH

Thanks!!!

fjgd `r Sys.Date()`