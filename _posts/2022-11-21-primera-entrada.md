---
layout: post
title: Sistemas de Recomendación y FAT-ML
---

# Qué es FAT-ML?

FAT-ML viene de la sigla en inglés "Fairness, Accountability, and Transparency in Machine Learning". El desarrollo de algoritmos de machine learning y su aplicación en el mundo real, provocan un impacto que en algunos casos puede llegar a ser negativo. En base a la problemática anterior, nacieron algunas agrupaciones como FAT-ML, que buscan entregar lineamientos y propuestas de regulación para evitar o mitigar efectos adversos provocados por utilizar soluciones derivadas de algoritmos de inteligencia artificial.

En palabras de la propia organización:

> *Algorithms and the data that drive them are designed and created by people -- There is always a human ultimately responsible for decisions made or informed by an algorithm. **"The algorithm did it"** is not an acceptable excuse if algorithmic systems make mistakes or have undesired consequences, including from machine-learning processes.*
> 
> (Los algoritmos y los datos que los impulsan, son diseñados y creados por personas: siempre hay un ser humano responsable en última instancia de las decisiones tomadas o informadas por un algoritmo. Decir que **"El algoritmo lo hizo"** no es una excusa aceptable si los algorítmicos cometen errores o tienen consecuencias no deseadas, incluido en los procesos de aprendizaje automático.)


A continuación revisaremos cada una de las siglas:

## Fairness: Justicia y Equidad

Se debe asegurar que las decisiones de un algoritmo de ML no generen discriminación o sesgo sobre un grupo específico basado en raza, sexo, identidad sexual, grupo socio-económico, nivel educacional, religión, nacionalidad u otros. En palabras de la agrupación, como desarrolladores o posibles entidades que tomarán decisiones basadas en recomendación de este tipo de algoritmos, deberíamos preguntarnos:

> *¿Existen grupos particulares que puedan verse favorecidos o perjudicados, en el contexto en el que se está desplegando, por el algoritmo / sistema que se está construyendo?*
> 
> *¿Cuál es el posible efecto perjudicial de la incertidumbre o los errores para los distintos grupos?*

## Accountability: Responsabilidad y Explicabilidad

Se debe asegurar que existe un organismo, institucionalidad o ente que se hace responsable ante los posibles impactos negativos de decisiones de un algoritmo de ML o sus mitigacione. Además, que tenga la obligación de reportar, explicat y justificar estas decisiones. Desde el punto de vista propuesto por FAT-ML, este punto debe considerar 5 aspectos claves:

- **Responsibility (Responsabilidad):** Se debe establecer claramente la intitución o ente a cargo de reparar porsibles efectos negativos de una decisión basada en algoritmos de ML.
- **Explainability (Explicabilidad):** Se debe garantizar que las decisiones de un algoritmo de ML son explicables tanto para usuarios como para terceros en términos no-técnicos.
- **Accuracy (Precisión):** Se debe respaldar la precisión de toda decisión basada en algoritmos de ML, y explicitar sus posibles fuentes de incertidumbre u error.
- **Auditability (Auditabilidad):** Se debe permitir y faciltar a terceros el supervisar y revisar el funcionamiento de un algoritmo de ML.
- **Fairness (Justicia y Equidad)** Basado en los temas descritos en el primer punto.


## Transparency: Transparencia.

Se espera que las características que afectan en la decisión de un algoritmo de ML sean visibles tanto para quienes lo usan, lo regulan y/o se ven afectados por estas decisiones. Esta es uno de los lineamientos más complicados en la actualidad con la masificación de algoritmos de Deep Learning con una enorme cantidad de parámetros (del orden de miles de millones), donde se dificulta el comprender a cabalidad el porqué el algoritmo toma una decisión o incluso, debido a la complejidad de la misma salida del algoritmo.

# Problemas de sesgo en Sistemas de Recomendación

La siguiente imagen [http://gendershades.org/overview.html] resume algunas de las amenazas de las decisiones de algoritmos de ML a nivel individual y social. 


<a href="url"><img src="https://i.dailymail.co.uk/i/pix/2018/02/12/20/4924BD1E00000578-0-image-a-21_1518465941000.jpg" align="center"></a>






## ¿Cómo pueden afectar estos sesgos a grupos específicos?

En particular, es de mi interés explorar el impacto de decisiones de sistemas de recomendación de ML a grupos LGBTQ+. 
Existen algunos ejemplos de cómo sistemas automatizados pueden terminar integrando sesgos a grupos minoritarios. Algunos ejemplos son:

- En 2019v

<blockquote class="twitter-tweet"><p lang="en" dir="ltr">I did the opposite or best I thought. Both just have random gameplay footage I had on my laptop. <a href="https://t.co/5Nu9WSi1l3">pic.twitter.com/5Nu9WSi1l3</a></p>&mdash; Sarah 🎃 (@ProdigyGirlYT) <a href="https://twitter.com/ProdigyGirlYT/status/1178719793869926405?ref_src=twsrc%5Etfw">September 30, 2019</a></blockquote> <script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

