---
layout: post
title: Sistemas Recomendadores - FAT-ML
---

La abundancia de los datos digitales en conjunto a la popularidad del uso de algoritmos de inteligencia artifical y machine learning (ML) cada vez más complejos y difíciles de explicar, nos ha llevado a preguntarnos ¿Cómo evitar que un sistema provoque un impacto negativo en su aplicación en el mundo real? ¿Cómo afecta esto al campo de los sistemas de recomendación?

# Qué es FAT-ML?

FAT-ML viene de la sigla en inglés "Fairness, Accountability, and Transparency in Machine Learning". El desarrollo de algoritmos de machine learning y su aplicación en el mundo real, provocan un impacto que en algunos casos puede llegar a ser negativo. En base a la problemática anterior, nacieron algunas agrupaciones como [FAT-ML](https://www.fatml.org/) , que buscan entregar lineamientos y propuestas de regulación para evitar o mitigar efectos adversos provocados por utilizar soluciones derivadas de algoritmos de inteligencia artificial.

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

Se debe asegurar que existe un organismo, institucionalidad o ente que se hace responsable ante los posibles impactos negativos de decisiones de un algoritmo de ML o sus mitigaciones. Además, que tenga la obligación de reportar, explicar y justificar estas decisiones. 

Desde el punto de vista propuesto por FAT-ML, esta "Accountability" debe considerar al menos 5 aspectos claves:

- **Responsibility (Responsabilidad):** Se debe establecer claramente la intitución o ente a cargo de reparar porsibles efectos negativos de una decisión basada en algoritmos de ML.
- **Explainability (Explicabilidad):** Se debe garantizar que las decisiones de un algoritmo de ML son explicables tanto para usuarios como para terceros en términos no-técnicos.
- **Accuracy (Precisión):** Se debe respaldar la precisión de toda decisión basada en algoritmos de ML, y explicitar sus posibles fuentes de incertidumbre u error.
- **Auditability (Auditabilidad):** Se debe permitir y faciltar a terceros el supervisar y revisar el funcionamiento de un algoritmo de ML.
- **Fairness (Justicia y Equidad)** Basado en los temas descritos en el primer punto.


## Transparency: Transparencia.

Se espera que las características que afectan en la decisión de un algoritmo de ML sean visibles tanto para quienes lo usan, lo regulan y/o se ven afectados por estas decisiones. Esta es uno de los lineamientos más complicados en la actualidad con la masificación de algoritmos de Deep Learning con una enorme cantidad de parámetros (del orden de miles de millones), donde se dificulta el comprender a cabalidad el porqué el algoritmo toma una decisión o incluso, debido a la complejidad de la misma salida del algoritmo.

# Problemas de sesgo en Sistemas de Recomendación

La siguiente imagen [fuente](http://gendershades.org/overview.html) resume algunas de las amenazas de las decisiones de algoritmos de ML a nivel individual y social. 


<a href="url"><img src="https://i.dailymail.co.uk/i/pix/2018/02/12/20/4924BD1E00000578-0-image-a-21_1518465941000.jpg" align="center"></a>






## ¿Cómo pueden afectar estos sesgos a grupos específicos?

En particular, es de mi interés explorar el impacto de decisiones de sistemas de recomendación de ML a grupos LGBTQ+. 
Existen algunos ejemplos de cómo sistemas automatizados pueden terminar integrando sesgos a grupos minoritarios. Algunos ejemplos son:

- En 2019, un grupo de creadores de contenido LGBTQ+ demandaron a YouTube por sistemáticamente desmonetizar a los videos de sus canales sin incumplir con las normativas del propio servicio, solo por su propio contenido. El cuál era categorizado como "contenido para adultos" o "sexual" pese a tener un caracter de entretención o educativo [Fuente: Vox.com](https://www.vox.com/culture/2019/10/10/20893258/youtube-lgbtq-censorship-demonetization-nerd-city-algorithm-report) [Fuente: BBC.com](https://www.bbc.com/news/technology-49369122).

Demostraron, por ejemplo que los siguientes videos era desmonetizados solo por sus títulos:

>
>- “Gay -and Lesbian Guide to Vienna - VIENNA/NOW”
>- “LGBT Tik Tok Compilation in Honor of Pride Month”
>- “Top 10 Lesbian Couples in Hollywood Who Got Married”
>- “Lesbian Princess”
>- “Lesbian daughters with mom”
>

Sin embargo, todos volvían a ser aptos para ser "monetizados" al momento de cambiar los términos LGBTQ+ de los títulos a palabras como “friend” y “happy”.

En casos más absurdos, se presentaron ejemplos en los cuales una usuaria subió un video con un gameplay sin mayor contenido, solo cambiando el título. Mientras el video titulado "Mi experiencia siendo una mujer hetero (heterosexual)" era monetizado, el titulado "LQBTQ y mi experiencia siendo lesbiana" era desmonetizado:


![chatGPT2](https://user-images.githubusercontent.com/42724306/208563191-017f6b2b-2ddc-4afe-ba6e-0fde72e43cfa.JPG)


![chatGPT1](https://user-images.githubusercontent.com/42724306/208563193-5f2161ec-f7fb-43db-8e93-92318a650291.JPG)


- En 2020, un artículo titulado *"Queer erasure: Internet browsing can be biased against LGBTQ people, new exclusive research shows"* [Fuente](https://journals.sagepub.com/doi/10.1177/0306422020917088) realizó un estudio sobre las noticias recomendadas por Google News, demostrando que un 46% de las noticias recomendadas sobre temática LGBTQ+ en su ventana de estudio correspondían a medios conservados (sinedo un 36%  medios cristianos), en contraste, solo un 4% provenía de noticias de medios liberales. Además, se identificó que pese a existir medios informativos exclusivamente de temática LGBTQ+, ninguno fue recomendado en el período estudiado.


- En 2022, un artículo titulado *"Echo Chambers, Rabbit Holes, and Algorithmic Bias: How YouTube Recommends Content to Real Users"* [Fuente](https://www.theregister.com/2022/10/18/youtube_algorithm_conservative_content/) [Fuente](https://csmapnyu.org/research/echo-chambers-rabbit-holes-and-algorithmic-bias-how-youtube-recommends-content-to-real-users) realizó un estudio sobre cómo, sin importar la ideología política original del usuario, YouTube terminaba recomendando contenido conservador. Llevando al usuario a una cámara de eco de contenido similar y cada vez más extremista.

Actualmente existen agrupaciones como [Queer in Ai](https://www.queerinai.com/) que buscan  generar conciencia sobre las implicancias de la IA/ML a la comunidad LGBTQ+. Que pueden sensibilizar a la población sobre este tipo de temáticas.

Es importante como desarrolladores ponernos en el lugar de quienes podrían verse afectados por las soluciones que proponemos y buscar formas de explicar (más allá de métricas de desempeño) el impacto de nuestras propuestas en el área de algoritmos de ML.

Es relativamente fácil quedarnos con la respuesta *"Es lo que propuso el algoritmo"* sin darnos la tarea de buscar los sesgos implícitos de nuestros datos, que vienen de nuestra propia sociedad. Es nuestro deber, como desarrolladores, buscar forma de mitigarlos, y de romper el ciclo.

J.J.R









