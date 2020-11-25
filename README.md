#Práctica final


Librerías: OS, sklearn, cv2, skimage

Entregar: código , análisis (comparativa de varias pruebas) 

-info: pensar en datos de entrada, con tantas filas como ejemplos....
      -array de etiquetas
	
 FASE 1

     ---Clasificación de señales--------------
           1. leer imagenes
	   2. Mismo size
	   3. Pensar Extracción de características (tipos de procesamiento)
	   4. Preprocesamiento
           5. Extracción de características
           6. Elección de modelo para clasificar

 FASE 2
            --Detector de señales : dime donde puede haber una---------- Size aprox de 100x100
            1. Queremos enseñar que es una señal y que no es.
            2.parches de 100x100 de 'no señales'. Somos encargados de generarlo . 
            3.Clasificador coge parches y determina si hay señal o no. 
              iterar sobre parches y 'marcar' aquello que sea una señal. Puede llamarse a clasificador de iter 1
           


PRERREQUISITOS 
           
    -¿Y en una imagen, dónde están las características?  
      OpenCV --> transformar size de imagenes, para que tengan el mismo.
      Pensar en pixeles como características puede ser erróneo: por magnitudes. No es lo mismo persona baja que pequeña,
      pero es persona. Influye iluminación. 
     ¿y si la imagen está girada? ---> fallo 

      (PENSAR EN ALG. DETECCION CARACTERISTICAS): se puede pensar en varias opciones. 
            1.Coger el histograma, normalizando previamente. Y primero una ecualizacion del histograma. (No mejor opción)
	    2. Algoritmo Hog (histograma de gradiente orientado) . Skimage (similar a skicitlearn). 
              -Divide la imagen en bloques, y en cada uno de ellos calcula magnitud y gradiente, creando histograma local. 
              - En círculo, en borde existe gradiente: a partir del histograma se discrimina  

Webpedia:
load imagenes:
	https://stackoverrun.com/es/q/8315597
