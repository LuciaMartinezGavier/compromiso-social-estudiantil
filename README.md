# Compromiso Social estudiantil
Se trata de una parte de un proyecto de producción de un bot (realizado con https://rasa.com/).

* Cantidad de horas estimadas: 16hs
* Cantidad de horas requeridas por CSE: 30-60hs
miercoles 4-4.30
## Tarea
Generar paráfrasis de párrafos informativos para que el bot no responda siempre lo mismo.

El objetivo es generar entre 15 y 20 párrafos por insecto y por planta.
Hacer 3 párrafos madre.

Escribir oraciones simples: sujeto verbo predicado 60-70 caracteres.
Hacer diferentes párrafos: más y menos técnicos.
Modelo para simplificar texto en español
### Insectos
Generar párrafos que respondan diferentes preguntas sobre un instecto particular. Y parafrasearlos.

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
* babosita del peral (caída la pag.)

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

### 4ta semana: Continuación párrafos madre
- [x] 30 min de reunión
- [x] Crear repositorio en GitHub
- Seguir con párrafos madre 
	+ [ ] Babosas
	+ [ ] Hormigas urbanas
+ [ ] Simplificar textos (con modelo de simplificación en español).
+ [ ] Agregar los párrafos madre más técnicos.
+ Cantidad total de horas utilizadas = 30min

### Nra semana: Generación de paráfrasis
+ [ ] 30' reunión
+ Generar paráfrasis automáticas

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



