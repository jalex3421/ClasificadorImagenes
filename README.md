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
	https://www.it-swarm-es.tech/es/python-2.7/leer-varias-imagenes-en-una-carpeta-en-opencv-python/1057086468/
	
modificar imagen:
	https://likegeeks.com/es/procesar-de-imagenes-en-python/
(info:
	https://www.pluralsight.com/guides/building-features-from-image-data-in-python
umbralizacion variable:
	http://acodigo.blogspot.com/2017/08/umbralizacion-adaptativa-con-opencv.html)
	
	NECESITMOS DIFERENTES TIPOS DE FEATURE EXTRACTION!!!!!!
	
feauture extraction:
	https://www.analyticsvidhya.com/blog/2019/08/3-techniques-extract-features-from-image-data-machine-learning-python/
	https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8117846
	
	TOP
		https://docs.opencv.org/3.4/db/d27/tutorial_py_table_of_contents_feature2d.html
		
Tipos de feature extraction:
	https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8117846
	
Hog:  https://scikit-image.org/docs/dev/auto_examples/features_detection/plot_hog.html

SHIFT:

KeyPoint and descriptors: https://dsp.stackexchange.com/questions/10423/why-do-we-use-keypoint-descriptors
SURF:
	In short, SURF adds a lot of features to improve the speed in every step.
	Analysis shows it is 3 times faster than SIFT while performance is comparable to SIFT.
	SURF is good at handling images with blurring and rotation, but not good at handling viewpoint change and illumination change.
	

