# Charla_v1

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
    nature:
      ratio: "16:9"
      highlightStyle: github
      highlightLines: true
      countIncrementalSlides: false
      
---
class: inverse
background-image: url("img/fallout.png")
background-size: contain

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


???

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
class: inverse
background-color: #0148A4

# De qué vamos a hablar?

```{r eval=FALSE, tidy=FALSE, echo = FALSE}
remotes::install_github("yihui/xaringan")
```

.pull-left[
<img src ="img/one-million.jpeg" height=475px>

]

.pull-right[

<img src="img/nivel-10.jpeg" height=350px>

]

---

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
background-image: url("img/gr2.png")
background-size: cover




---
class:inverse
background-color:#1B9BBB


# La historia de la IA se puede resumir en 3 etapas



.pull-left[

Three major eras in AI development:

- 1950s-1970s: Foundational development with rule-based systems like MYCIN and Eliza chatbot

- 1970s-2000s: "AI winter" period with limited funding, followed by renewed interest with expert systems

- 2000s-2020: Explosive growth with deep learning, natural language processing, and cloud-based applications

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



- `r fa("question", fill = "blue")` **Qué era la inteligencia**

- 1943 - primer modelo matemático de una neurona (neurocientífico Warren McCullogh y el lógico Walter Pitts)
  - idea revolucionaria: unidades muy simples pueden computar cualquier función lógica

- 1950 - Turing (pueden pensar las máquinas)
  - <b>juego de la imitación</b>

- 1951 - primera máquina de red neuronal (Marvin Misnky/Dean Edmonds) que simulaba una rata encontrando el camino por un laberinto
  - <b>Snarc</b> Stochastic Neural Analog Reinforcement Computer 

- 1956 - conferencia de Dartmouth --> se acuña el término de <b>Inteligencia Artificial</b>

- 1957 - avance definitivo <b>Perceptron</b> de Frank Rosenblat, aprendía a reconocer patrones



???
el SNARC era un dispositivo analógico formado por 40 tubos de vacío, resistencias y condensadores, ensamblados para representar nodos y conexiones similares a las neuronas del cerebro humano. Su objetivo no era realizar cálculos a gran velocidad, sino imitar el modo en que los organismos aprenden a partir de la experiencia.
1951 – SNARC Maze Solver – Minsky / Edmonds (American)

In 1951 Marvin Minsky teamed with Dean Edmonds build the first artificial neural network that simulated a rat finding its way through a maze.

They designed the first (40 neuron) neurocomputer, SNARC (Stochastic Neural Analog Reinforcement Computer), with synapses that adjusted their weights (measures of synaptic permeabilities) according to the success of performing a specified task (Hebbian learning) The machine was built of tubes, motors, and clutches, and it successfully modeled the behavior of a rat in a maze searching for food.

As a student, Minsky had dreamed of producing machines which could learn by providing them with memory "neurones" connected to "synapses"; the machine would also have to possess past memory in order to function efficiently when faced with different situations.

In 1951 the "machine" was born, consisting of a labyrinth of valves, small motors, gears and wires linking up the various "neurones". Some of these wires were connected up at random to the various memory banks in order to achieve a degree of causality of events. The reason such a machine had been put together was to try and find the exit from a maze where the machine would play the part of a rat whose progress would be monitored on a light network.

When the system was completed it was possible to follow all the movements of the 'rat' within the maze and it was only through a design fault that it was found more than one 'rat' could be introduced which would then interact together. After various casual attempts the rats started 'thinking' on a logical basis helped along by reinforcement of correct choices made and the more advanced rats would then be followed by the ones left behind. This first practical example, built by Minsky with the help of Dean Edmonds, also included numerous casual connections between its various 'neurones', acting like a sort of nervous system able to overcome any eventual information interruption due to one of the neurones failing.


---
background-image: url("D:/OBSIDIAN_notes_2/charla_IA_unican/img/MYCIN.webp")
background-position: 95% 5%
background-size: 200px

# Primeros sistemas expertos (1970s)

- DECsystem-10
  - se pasó de decenas de miles de transistores a 1000-50.000 millones
  
- MYCIN, sistema de diagnóstico y tratamiento de infecciones bacterianas (rendimiento comparable a médicos expertos)

- Intenist 1, era más complejo

- CASNET, en glaucoma (tenía en cuenta las causas, no sólo los síntomas, razonamiento basado en modelos)

---
class: inverse
background-image: url("img/AI_winters.jpg")
background-position: 95% 5%
background-size: 250px

# Primer invierno de la IA (1980s)

- principales cuellos de botella

- Ingeniería del conocimiento
  - extracción y codificación del conocimiento para ser usado por los sitemas expertos
  - limitado poder computacional de la época
- conocimiento tácito de expertos -> reglas explícitas, no usa un si-entonces


Hay una crisis de confianza.
Segundo invierno a principios de los 90s, por ineficiencia de las NN.


---
class: inverse
background-image: url("img/AI_winters.jpg")
background-position: 95% 5%
background-size: 250px

# Tras un segundo invierno<br/> (inicios 1990s)

- sobre todo por el desvanecimiento del gradiente, las capas más profundas no aprendían correctamente, impidiendo que ella misma siga aprendiendo

- entrenar estas redes era lento

- se cambió el foco hacia aprendizajes más pragmáticos --> Aprendizaje Automático (ML)
  sistemas basados en regla --> Aprendizaje donde los algoritmos aprenden patrones directamente de los datos, con métodos más robustos (SVM o árboles de decisión)
  

En segundo plano se construyó la infraestructura hacia el aprendezaje profundo (DL)


---

# Transición hacia el aprendizaje automático, ML (1990s-2012)

De archivos en papel a repositorios digitales inmensos

Ley de Moore



---

# Finales de los 2000s

Más datos, más capacidad de computación.

MYCIN (1972) &rarr; CAD(2006)

--

## Radiómica (2010)

Las imágenes médicas contienen información mucho más allá de lo que el ojo humano puede percibir.

Extracción de cientos/miles de características de la imagen, para construir modelos predictivos (sobre todo oncología)

---

# La era del aprendizaje profundo, DL (2012-presente)

Combinación de tres factores

- el algoritmo de retropropagación (backpropagation)
  -desvanecimiento del gradiente
  
- GPUs - unidades de procesamiento gráfico

- datos masivos - IMAGENET

--

AlexNet (2012

disminuyo la tasa de error a más de la mitad, respecto al segundo




---

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
class: inverse

background-color:#E64626

# Primeras aplicaciones del DL

Ca piel
Retinopatía diabetica

--

Arquitectura U-Net (2015)

<!-- incluir img -->

--

GANs (2014)

--

Radiómica potenciada por el DL


--

### U-Net (2015)

--

### Redes Generativas Antagónicas (GANs)

--

### Radiómica (2010)

--

### PNL (Procesamiento del Lenguaje Natural)

Hay arquitecturas novedosas, el gran avance son los <b>Transformers</b>

<img src = "img/transformer_arquitecture.png">

Su innovación clave es el <b>mecanismo de atención</b>: permite sopesar las diferentes palabras en un texto capturando contexto y relaciones a distancia

Esto ha llevado al desarrollo de los <b>modelos fundacionales</b> (ej.: los GPTs)

Lo más relevante, aunque están pre-entrenados con gran cantidad de datos de internet, pueden ser perfeccionados con facilidad, mediante <b>fine-tunning</b> (ajuste fino).

<img src = "img/LLM_fine-tuning.png">

---

background-color:#FCE300

# Como resumen

.pull-left[
- hemos pasado de la lógica de un médico con reglas fijas &rarr; sistemas que aprenden <b>patrones complejos</b> a partir de cantidades ingentes de <b>datos</b>

<img src ="img/conclusion.png"width = 350px>

]

.pull-right[
- el progreso ha sido superar cuellos de botella sucesivos<br/> .content-box-red[razonamiento&rarr;conocimiento&rarr;computación]

- el desafio actual es .content-box-red[cómo integrar en los flujos actuales de trabajo estas herramientas] de forma
  - segura
  - ética
  - eficaz
]



---
class: inverse
background-color: #1B9BBB
background-image: url("img/caja-negra3.png")
background-position: 95% 5%
background-size: 200px



# Incorporación de la IA a la relación médico-paciente
## Dónde estamos?

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

| Término                      |                          Definición                          |                          Relevancia                          |
| :--------------------------- | :----------------------------------------------------------: | :----------------------------------------------------------: |
| Human-in-the-loop            | la IA emite recomendaciones<br/>la decisión final es humana  |        refuerza responsabilidad médica y la confianza        |
| IA autónoma                  | decisiones diagnósticas/terapéuticas sin intervención humana | reduce el contacto directo<br/>genera dudas de responsabilidad |
| XAI                          |        decisiones de la IA interpretadas y explicadas        |                  facilita la transparencia                   |
| Fatiga de alertas            |     exceso de notificaciones<br/>con pérdida de atención     |    reduce la seguridad y<br/>eficacia de la comunicación     |
| Ruido algorítmico            |              información irrelevante o errónea               |      aumenta la confusión<br/>dificulta la comunicación      |
| Sesgo algorítmico            | datos de entrenamiento<br/>que conducen a un error sistemático |        genera inequidades<br/>deteriora la confianza         |
| Autonomía del paciente       |                      derecho a decidir                       |          explicar el papel de la IA<br/>y opciones           |
| Toma de decisiones aumentada | capacidad analítica aumentada por la IA<br/>se mantiene supervisión humana | mejora calidad de la consulta<br/>y percepción de competencia |
| Validación clínica           |  beneficio y seguridad demostrados<br/>en la práctica real   |                  garantiza evidencia sólida                  |
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

# la regla de los tres segundos


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

- `r fa("robot")` CNN en imagen
  - clasifican y segmentan lesiones con precisión submilimétrica

- `r fa("robot")` Modelos de secuencia (LSTM, GRU)
  - en monitorización y predicción del deterioro

- `r fa("robot")` Transformadores multimodales
  - combinan datos clínicos, imagen y texto

- .content-box-grey[Tipo de arquitectura &rarr; condiciona interpretabilidad y potencial de error]



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

<img src="img/geoffrey-hinton-cientifico-inteligencia-artificial.webp" height=250px>
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

- .content-box-yellow[transparencia y explicabilidad] proporcional al riesgo clínico


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
class:inverse
background-image: url("img/replies.png")
background-size:contain

---

FINISH

Thanks!!!

fjgd `r Sys.Date()`

# Bibliografía
1. https://libros.catedu.es/books/la-ia-en-educacion-una-aproximacion-practica/page/unidad-21-de-que-estamos-hablando-concepto-y-definiciones-de-ia
2. 