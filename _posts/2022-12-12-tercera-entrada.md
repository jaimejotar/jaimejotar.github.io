---
layout: post
title: Sistemas Recomendadores - Desafíos al futuro.
---

Los sistemas recomendadores se utilizan en una amplia variedad de aplicaciones, como la recomendación de productos en línea (Amazon, eBay, Mercado Libre, otras tiendas digitales y publicidad de tiendas en redes sociales) o en la personalización de contenido en plataformas de medios y redes sociales (nuestro "feed" de Twitter, Facebook, Instagram, Twitter). Aún existen múltiples desafíos en el campo de sistemas recomendadores. Limitemos a tres de los más importantes:

## 1. Calidad de los datos.

Uno de los principales desafíos es la falta de datos de calidad. Muchos sistemas recomendadores se basan en el uso de datos de interacción del usuario (como clics en item específicos o acciones de compra), para entrenar y mejorar sus modelos. Sin embargo, a veces puede ser difícil obtener datos suficientes y de calidad para entrenar estos modelos de manera efectiva. Además, los datos a menudo pueden ser incompletos o inexactos, lo que puede afectar la precisión y la efectividad de las recomendaciones.


## 2. Sobre-personalización (Sesgo por confirmación)

Los sistemas recomendadores a menudo se basan en la personalización para proporcionar recomendaciones relevantes y personalizadas para cada usuario. Sin embargo, es posible que algunos sistemas proporcionen demasiada personalización, lo que puede llevar a una "burbuja" o "cámara de eco" en la que el usuario solo ve contenido que coincide con sus intereses y prejuicios preexistentes. Esto puede limitar la exposición del usuario a nuevas ideas y perspectivas y puede tener implicaciones negativas para la sociedad en general.

## 3. Sesgos en datos y modelos.

Los sistemas recomendadores a menudo se basan en datos históricos para proporcionar recomendaciones, lo que puede llevar a sesgos y discriminación en las recomendaciones. Por ejemplo, si un sistema recomendador se entrena en datos históricos que reflejan la discriminación de género, es posible que proporcione recomendaciones discriminatorias para los usuarios. Es importante tener en cuenta estos sesgos y trabajar para eliminarlos de los datos y los modelos de sistemas recomendadores.

# ¿Cómo podemos combatir los sesgos?

Muchos sesgos se originan a partir de los mismos datos de entrenamiento. Como el origen de los datos y contenido proviene del mundo actual ( e histórico), se traspasan sesgos que provienen de los propios datos, ya que lamentablemente nuestra historia y nuestra sociedad actual, es "sesgada".

Específicamente para Sistemas Recomendadores existen desafíos inherentes a la propia tarea. Como lo explica el artículo: [*"(Chan J. et al. ) Bias and Debias in Recommender System: A Survey and Future Directions"*](https://arxiv.org/pdf/2010.03240.pdf) existen loops dentro del mismo sistema que amplifican el sesgo del sistema recomendador, pero que pueden tener posibles soluciones sobre todo en publicaciones que se han ido incrementando en los últimos 5 años.

![chatGPT3](https://user-images.githubusercontent.com/42724306/208569949-3d947fae-266d-44c4-94cb-4a830501edc4.JPG)


- **Del usuario a los datos**: Sesgo de selección (por el interés del usuario), Sesgo de Exposición (por popularidad de un item), Sesgo de conformidad (por conformidad al contenido recomendado), Sesgo por posicionamiento (por confianza del usuario en el top propuesto, no promueve su exploración de nuevos contenidos). Estos sesgos pueden ser enfrentados mediante modelos que incluyan la veracidad de un contenido, que incluyan un "Propensity Score" y modelando los efectos de popularidad de los contenidos.
- **De los datos al modelo**: Sesgo inductivo incluido por los desarrolladores. En teoría, corresponde a soluciones para mejorar la generalización y rendimiento de los modelos.
- **Del modelo al usuario**: Sesgo por popularidad y sesgo por inequidad. Estos problemas generalmente son generados por el propio algoritmo debido a su entrenamiento y el desbalance de los datos. Posibles soluciones implican un conocimiento sobre los datos de entrenamiento para rebalanceo, regularización y aprendizaje adversario.
- **Sistema completo**: Sesgo retroalimentado. Un sesgo retroalimentado por la triangulación, decisión del usuario, datos de entrenamiento del modelo y recomendación del modelo. Para "romper" este loop, es posible incluir recomendaciones aleatorias y aprendizaje reforzado.

# Comentarios finales.

Existen desafíos abiertos para resolver en torno a los Sistemas Recomendadores, más aún, con la popularidad de algoritmos basados en redes neuronales profundas que funcionan como "Cajas Negras" que son difíciles de explicar y visualizar. Sin embargo, hay agrupaciones que han empezado a generar conciencia sobre el impacto que tienen o podrían llegar a tener estos algoritmos en nuestro día a día. Tener conciencia sobre estas problematicas, como desarrolladores es el primer paso, tenemos que ser concientes y buscas posibles soluciones antes de que nuestros desarrollos puedan generar un impacto negativo en el mundo real.

Es nuestro deber como desarrolladores, buscar generar soluciones que no generen un impacto negativo en grupos de nuestra sociedad.

_J.J.R_
