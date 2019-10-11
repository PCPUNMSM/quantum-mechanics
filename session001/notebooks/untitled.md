# Una introducción simple a los *Métodos Numéricos* para `@mistyblunch`

Hace ya algunos años que debí de escribir estas notas. Como dicen "más vale tarde que nunca", aquí vamos. Lo siento, @mistyblunch, por tanto retraso.

Al momento que escribo esto, @mistyblunch ya está en la universidad; posiblemente en su 2<sup>do</sup> o 3<sup>er</sup> ciclo. Pero cuando quise escribir esto, originalmente, recién salía de la escuela. Espero que estas notas cumplan con otros jóvenes lo que esperaba que cumplieran con @mistyblunch: Motivar su curiosidad por la mátematica, la computación y la física.

## Definiciones simples

De la escuela conocemos las definiciones de velocidad y aceleración:

1. *La **velocidad** es la [tasa de] variación de la posición respecto del tiempo*
    
$$
\mathbf{v} = \frac{\mathbf{x}_f - \mathbf{x}_i}{t_f - t_i}
$$


2. *La **aceleración** es [tasa de] la variación de la velocidad respecto del tiempo*

$$
\mathbf{a} = \frac{\mathbf{v}_f - \mathbf{v}_i}{t_f - t_i}
$$

Ademas tambien nos enseñaron la llamada "Segunda ley de newton" en forma de ecuación

$$
\mathbf{F} = m\mathbf{a}
$$

Resulta fantástico saber que con estas tres expresiones y un poco de creatividad y manipulaciones algebraicas podemos precedir el futuro!

## ¿Qué son y para que nos sirven los modelos fisicos?

La verdad es que la llamada Segunda Ley de Newton es una relacion universal que nos dice como se mueve el mundo. Podemos obtener toda clase de resultados a partir de ella. Tal vez el mas importante es la predicion del futuro.

En la expresion

$$
m\mathbf{a} = \mathbf{F}
$$

sustituimos lo que entendemos como la "definición" de la aceleración

$$
\frac{\mathbf{v}_f - \mathbf{v}_i}{t_f - t_i} = \frac{\mathbf{F}}{m}
$$

de donde despejamos los $\mathbf{v}_f$

$$
\mathbf{v}_f = \mathbf{v}_i + \frac{\mathbf{F}}{m}\left(t_f - t_i\right)
$$

Tambien despejamos $x_f$ en la "definición" de velocidad de modo que

$$
\mathbf{x}_f = \mathbf{x}_i + \mathbf{v}\left(t_f - t_i\right)
$$

En ambas expresiones consideremos que $t_i = 0$, $t_f = t$, $\mathbf{x} = \mathbf{x}_f$ y $\mathbf{v} = \mathbf{v}_f$ de forma que obtenemos el par de ecuaciones

$$
\mathbf{v} = \mathbf{v}_i + \frac{\mathbf{F}}{m} t
$$

$$
\mathbf{x} = \mathbf{x}_i + \mathbf{v} t
$$

Estas expresiones nos permiten conocer $\mathbf{x}$ y $\mathbf{v}$ en cualquier instante $t$ si es que conocemos $\mathbf{x}_i$ y $\mathbf{v}_i$. Es decir, si conocemos los valorezs de $\mathbf{x}_i$ y $\mathbf{v}_i$, ademas de la fuerza $\mathbf{F}$, podemos determinar $\mathbf{x}$ y $\mathbf{v}$ en cualquier instante $t$: Podemos predecir el futuro.

En honor a la verdad de la ciencia debemos decir que lo enucniado anteriomente no es cierto, pero constituye una aproximacion bastante razonable para intervalos de tiempo muy pequeños, y haciendo uso de estos intervalos pequeños podemos avanzar paso a paso hasta llegar al tiempo de deseamos.

Este conocimiento del futuro ($\mathbf{x}$ y $\mathbf{v}$), basado en la evidencia actual ($\mathbf{x}_i$ y $\mathbf{v}_i$) constituye el fin ultimo de un modelo fisico, que no es otra cosa que un caso particular de la segunda ley de newton en donde conocemos como se comporta $\mathbf{F}$

## Ejemplo 1: Lanzamiento de proyectiles

Apliquemos todo lo dicho anteriormente en un ejemplo clasico y sencillo: el movimiento parabolico.