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

- En 2019, un grupo de creadores de contenido LGBTQ+ demandaron a YouTube por sistemáticamente desmonetizar a los videos de sus canales sin incumplir con las normativas del propio servicio, solo por su propio contenido. El cuál era categorizado como "contenido para adultos" o "sexual" pese a tener un caracter de entretención o educativo [https://www.vox.com/culture/2019/10/10/20893258/youtube-lgbtq-censorship-demonetization-nerd-city-algorithm-report] [https://www.bbc.com/news/technology-49369122].

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


- En 2020, un artículo titulado *"Queer erasure: Internet browsing can be biased against LGBTQ people, new exclusive research shows"* [https://journals.sagepub.com/doi/10.1177/0306422020917088] realizó un estudio sobre las noticias recomendadas por Google News, demostrando que un 46% de las noticias recomendadas sobre temática LGBTQ+ en su ventana de estudio correspondían a medios conservados (sinedo un 36%  medios cristianos), en contraste, solo un 4% provenía de noticias de medios liberales. Además, se identificó que pese a existir medios informativos exclusivamente de temática LGBTQ+, ninguno fue recomendado en el período estudiado.


- En 2022, un artículo titulado *"Echo Chambers, Rabbit Holes, and Algorithmic Bias: How YouTube Recommends Content to Real Users"* [https://www.theregister.com/2022/10/18/youtube_algorithm_conservative_content/] [https://csmapnyu.org/research/echo-chambers-rabbit-holes-and-algorithmic-bias-how-youtube-recommends-content-to-real-users] realizó un estudio sobre cómo, sin importar la ideología política original del usuario, YouTube terminaba recomendando contenido conservador. Llevando al usuario a una cámara de eco de contenido similar y cada vez más extremista.

Actualmente existen agrupaciones como Queer in Ai [https://www.queerinai.com/] que buscan  generar conciencia sobre las implicancias de la IA/ML a la comunidad LGBTQ+. Que pueden sensibilizar a la población sobre este tipo de temáticas.


# ¿Cómo combatir los sesgos?

Muchos sesgos se originan a partir de los mismos datos de entrenamiento. Como el origen de los datos y contenido proviene del mundo actual ( e histórico), se traspasan sesgos que provienen de los propios datos, ya que lamentablemente nuestra historia y nuestra sociedad actual, es "sesgada".

Específicamente para Sistemas Recomendadores existen desafíos inherentes a la propia tarea. Como lo explica el artículo: *"(Chan J. et al. ) Bias and Debias in Recommender System: A Survey and Future Directions"* [https://arxiv.org/pdf/2010.03240.pdf] existen loops dentro del mismo sistema que amplifican el sesgo del sistema recomendador, pero que pueden tener posibles soluciones sobre todo en publicaciones que se han ido incrementando en los últimos 5 años.

![chatGPT3](https://user-images.githubusercontent.com/42724306/208569949-3d947fae-266d-44c4-94cb-4a830501edc4.JPG)


- **Del usuario a los datos**: Sesgo de selección (por el interés del usuario), Sesgo de Exposición (por popularidad de un item), Sesgo de conformidad (por conformidad al contenido recomendado), Sesgo por posicionamiento (por confianza del usuario en el top propuesto, no promueve su exploración de nuevos contenidos). Estos sesgos pueden ser enfrentados mediante modelos que incluyan la veracidad de un contenido, que incluyan un "Propensity Score" y modelando los efectos de popularidad de los contenidos.
- **De los datos al modelo**: Sesgo inductivo incluido por los desarrolladores. En teoría, corresponde a soluciones para mejorar la generalización y rendimiento de los modelos.
- **Del modelo al usuario**: Sesgo por popularidad y sesgo por inequidad. Estos problemas generalmente son generados por el propio algoritmo debido a su entrenamiento y el desbalance de los datos. Posibles soluciones implican un conocimiento sobre los datos de entrenamiento para rebalanceo, regularización y aprendizaje adversario.
- **Sistema completo**: Sesgo retroalimentado. Un sesgo retroalimentado por la triangulación, decisión del usuario, datos de entrenamiento del modelo y recomendación del modelo. Para "romper" este loop, es posible incluir recomendaciones aleatorias y aprendizaje reforzado.

## Comentarios finales.

Existen desafíos abiertos para resolver en torno a los Sistemas Recomendadores, más aún, con la popularidad de algoritmos basados en redes neuronales profundas que funcionan como "Cajas Negras" que son difíciles de explicar y visualizar. Sin embargo, hay agrupaciones que han empezado a generar conciencia sobre el impacto que tienen o podrían llegar a tener estos algoritmos en nuestro día a día. Tener conciencia sobre estas problematicas, como desarrolladores es el primer paso, tenemos que ser concientes y buscas posibles soluciones antes de que nuestros desarrollos puedan generar un impacto negativo en el mundo real.

Es nuestro deber como desarrolladores y como personas, buscar generar soluciones que no generen un impacto negativo en grupos de nuestra sociedad.

J.J.R






