Se trata de una parte de un proyecto de producción de un bot (realizado con https://rasa.com/).

* Cantidad de horas estimadas: 16hs
* Cantidad de horas requeridas por CSE: 30-60hs
miercoles 4-4.30

## Tarea
Generar paráfrasis de párrafos informativos para que el bot no responda siempre lo mismo.

Escribir oraciones simples: sujeto verbo predicado 60-70 caracteres.
Hacer diferentes párrafos: más y menos técnicos.
Mínimo 4 textos (párrafos combinados) por tema (insecto): agregar y sacar párrafos madre/paráfrasis.

### Insectos
Generar párrafos que respondan diferentes preguntas sobre un insecto particular. Y parafrasearlos.

Los párrafos deben variar en la pregunta que responden y en el estilo de escritura: amigable, formal, directo, con emojis.

#### Insectos considerados
**Los que son plaga en la huerta son:**
* Tijereta
* Pulgones 
* Babosas
* Orugas
* Pilme
* Hormigas

**En frutales:**
* babosita del peral

### Plantas
Generar párrafos de propiedades nutritivas que no superen los 256 caracteres (se puede revisar esta cota).


## Facts útiles
***
Una tarea esencial en el área de procesamiento de lenguaje natural es la traducción automática. Y la tarea de generar paráfrasis es parecida a la traducción.
Se trata de una oración que transmite el mismo mensaje pero con otras palabras (analogía con una traducción al mismo idioma).

Se puede hacer un proceso así:
Español -> inglés > español

La IA no es perfecta y a veces genera oraciones con datos que no estaban ahí en un principio, eso es un fenómeno que se llama *alucinación*.

Es nuestra tarea en este proyecto revisar los párrafos generados para filtrar información falsa si es que la hay.


Los *modelos generativos* sirven para hacer paráfrasis. Son simples de usar con notebooks de python

En algunos se puede modificar el parámetro *temperature* (que determina cuánto varía del párrafo original).

Hay algunas palabras que son claves y no deben modificarse. Para asegurarse que eso no va a cambiar se puede reemplazar por algo como `XXXX` y luego volver a reemplazarlo por la palabra original.

***
En las Redes neuronales cada oración es representada por un vector de cientos de dimensiones y se van agrupando las oraciones similares de acuerdo a la cercanía en ese espacio vectorial. De esta manera el bot puede determinar de qué tema se está hablando y envía la respuesta que más cercana esté en ese espacio.
***

## To do list
<!--Las horas se cuentan desde el comienzo de una weekly hasta la siguiente-->
### 1ra semana: Exploración
+ [x] 30' reunión
+ [x] Inscribirse en el compromiso social estudiantil
+ [x] Explorar herramientas
+ Cantidad total de horas utilizadas = 3hs

### 2da semana: Párrafos madre
+ [x] 1hs reunión
+ [x] Plantear preguntas, datos que deben estar si o si
+ [x] Empezar a escribir párrafos madre a mano (pulgones)
+ Cantidad total de horas utilizadas = 2hs 30min

### 3ra semana: Continuación párrafos madre
- [x] 30 min de reunión
- Seguir con párrafos madre 
	- [x] Tijeretas
	- [x] Pilme
	+ [x] Orugas
+ Cantidad total de horas utilizadas = 3hs

### 4ta y 5ta semana: Continuación párrafos madre
- [x] 30 min de reunión
- [x] Crear repositorio en GitHub
- Seguir con párrafos madre 
	+ [x] Babosas
	+ [x] Hormigas urbanas
	+ [x] babosita del peral
+ [x] Simplificar textos (con modelo de simplificación en español).
+ Cantidad total de horas utilizadas = 2hs 30min


### 6ta semana: Generación de paráfrasis
+ [x] 30' reunión
- [x] Escribir script para generar paráfrasis automáticas: Output: texto final que van a leer los usuarios.

+ Cantidad total de horas utilizadas = 3hs

### 7ma semana:
- [x] 30' reunion
- [x] Enviar párrafos madre a ingenieros para que verifiquen que estén bien.
- [??] Hacer un diccionario de sinónimos para generar oraciones con la misma semántica. (Ver librería `spacy`).
- [x] Hacer paráfrasis de pulgones con generadores de paráfrasis de internet
- Cantidad total de horas utilizadas = 2hs

### 8va semana:
- [x] 30' reunión
- [ ] Hacer paráfrasis de los demás insectos cuando estén verificados los párrafos madre
	- Usar modelo de Guido también

### Nra semana: Evaluación de paráfrasis
+ [ ] 30' reunión
+ Valuación de paráfrasis (1hs máx)
	+ Mantuvo la semántica
	+ Suena bien en español
	+ Tiene coherencia interna
+ Segunda prioridad: hacer textos más formales

## Links útiles

**Manual de Compromiso Social estudiantil:**
https://www.unc.edu.ar/sites/default/files/MANUAL%20CSE%20v1%20%281%29.pdf

**Modelos paráfrasis español:**

1. https://huggingface.co/mrm8488/bert2bert_shared-spanish-finetuned-paus-x-paraphrasing

    Este es un notebook para que vean como se corre en python:
    https://colab.research.google.com/drive/1LgJPptiKbaRdcM7DMaxHxHSBIUOpIFfl?usp=sharing

2. https://huggingface.co/Prompsit/paraphrase-roberta-es

**Modelo paráfrasis de preguntas en inglés:**
1. https://huggingface.co/ramsrigouthamg/t5_paraphraser

**Modelo paráfrasis en inglés:**
1. https://huggingface.co/ramsrigouthamg/t5-large-paraphraser-diverse-high-quality

**Tools de paráfrasis en español sin fuentes:**
https://www.paraphraser.io/ // no publican el modelo :/

https://parafrasear.org/

https://www.editpad.org/tool/es/paraphrasing-tool

https://parafrasear.es/


**Recetario con información nutricional de plantas:**
* https://drive.google.com/file/d/1OwGsmHz9bkr9bFmQbrxCQl_fsez9ZCUA/view?usp=sharing

**Cuadernillos de los insectos**
https://inta.gob.ar/documentos/serie-de-divulgacion-sobre-insectos-de-importancia-ecologica-economica-y-sanitaria



***
Las paráfrasis del modelo  https://huggingface.co/mrm8488/bert2bert_shared-spanish-finetuned-paus-x-paraphrasing no fueron  muy buenas (ejemplos de un par de paráfrasis sobre hormigas).

*Original*:
+ La longitud normal de una hormiga es de 1 a 5 mm, aunque se han llegado a descubrir **hormigas** de hasta 30 mm (no en la región patagónica).  

*Paráfrasis*:  
+ La longitud normal de una hormiga es de 1, 5 mm, aunque se han llegado a descubrir **Lucy** de hasta 30 mm ( no en la región patagónica ).
+ La longitud normal de una hormiga es de 1 a 5 mm, aunque se han llegado a descubrir **concreto** de hasta 30 mm ( no en la región patagónica ).

*Original:*
+ Tienen cabeza grande, antenas articuladas, poderosas mandíbulas y tres regiones corporales (cabeza, tórax y abdomen). En el extremo último del abdomen se puede encontrar el **aguijón**.  

*Paráfrasis:*  
+ Tienen cabeza grande, antenas articuladas, poderosas mandíbulas y tres regiones corporales ( cabeza, tórax y abdomen ), en el extremo último del abdomen se puede ser la **espiijón**.
+ Tienen una cabeza grande, antenas articuladas, poderosas mandíbulas y tres regiones corporales ( cabeza, tórax y abdomen ), en el extremo final del abdomen se puede encontrarse el **Drijón**.

*Original:* 
+ Las hormigas pueden **dañar aparatos** **electrónicos** y materiales estructurales, tales como maderas en vigas o ventanas, revestimientos y **cimientos**.

*Paráfrasis:*
+ Las hormigas pueden **dañartrones** electrónicos y materiales estructurales, como maderas en vigas o ventanas, revestimientos y motores. **É É sk X / swnship**
+ Las hormigas pueden dañar **Electronicas** y materiales estructurales, como maderas en vigas o ventanas, revestimientos y motores. **É É sk X / swnship**
+ Las hormigas pueden dañar **Electronicas** y materiales estructurales, como maderas en vigas o ventanas, revestimientos y motores. **É / sk X / swnship**



