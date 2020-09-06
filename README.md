# ISDB-T
Trabajo final presentado en la materia Radiodifusión Sonora y Televisiva.

En este repositorio encontrarán una presentación de PowerPoint con la explicación de la norma ISDB-T ABNT NBR 15601. En una primera parte se explica el funcionamiento de OFDM,
como base de este sistema de transmisión. Luego se explica el sistema de transmisión propiamente, desde que ingresamos con archivos MPEG, pasando por la división en capas
jerárquicas, codificación, modulación, hasta lograr una señal de salida, la cual es enviada a la antena para ser transmitida a través del aire. Finalmente, se deducen los valores
expuestos en cuatro de las tablas más representativas de la norma.

Por otra parte, encontrarán también una simulación en python (archivo .ipnb) de los tres modos de operación de ISDB-T, su modulación, inserción del intervalo de guarda, función
de las portadoras piloto para estimar los efectos del canal de comunicaciones, entre otros. Al final de la misma encontrarán las respectivas mediciones de PAR y CCDF. Para poder
la simulación completa, con las imágenes correspondientes es recomendable descargar el repositorio completo y abrir el archivo .ipnb con Jupyter Notebook.

Por último, encontrarán también una simulación de GNURadio, basada en los proyectos publicados por @git-artes: gr-isdbt y gr-mer, en los que se muestra el funcionamiento del
sistema de transmisión según la norma mencionada anteriormente, incluyendo los bloques correspondientes a la codificación, modulación, separación en capas jerárquicas, entre otros.
Se aplican perturbaciones a las señales obtenidas mediante los bloques HW Impairments y Channel Model, y luego se mide el MER. De esta manera se pueden sacar conclusiones acerca de
la variación del MER frente a las mismas. Se agregó al trabajo realizado por @git-artes la implementación de las tres máscaras propuestas por la norma brasilera ISDB-T, para
corroborar que la señal obtenida se encuentre dentro de los parámetros solicitados.

Una mejora que podría realizarse a futuro, sería reimplementar la simulación de GNURadio en WX GUI, en lugar de hacerlo con QT GUI. Con este último, encontré que al agregar
perturbaciones a la señal, la constelación sólo se llena de ruido y no se comporta como indica la teoría. Hice algunas pruebas con WX GUI y la constelación muestra los efectos
esperados.
