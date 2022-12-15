# PI02_DataScience
Este es un proyecto hecho por Martín Eluney Gómez Piñeiro, para el curso de Data Scients de Henry en la cohorte 5.
En este proyecto se me dieron las siguientes pautas a seguir:

# **Problematica**
Un importante Centro de Salud lo ha contratado con el fin de poder predecir si un paciente tendrá una estancia hospitalaria prolongada o no, utilizando la información contenida en el dataset asociado, la cual recaba una muestra histórica de sus pacientes, para poder administrar la demanda de camas en el hospital según la condición de los pacientes recientemente ingresados.

Para esto, se define que un paciente posee estancia hospitalaria prolongada si ha estado hospitalizado más de 8 días. Por lo que debe generar dicha variable categórica y luego categorizar los pacientes según las variables que usted considere necesarias, justificando dicha elección.

# **PRealizacion del proyecto**
**EDA**

+ Primero lei los dos archivos CSV con ayuda de la libreria de Python pandas y cree un dataframe para cada uno.

+ Luego dí un primer vistazo a los datos, columnas y filas, para así tener una idea general del contenido de los datasets.

+ Busque valores nulos (no habia).

+ |Mire los valores unicos de cada columna para darme una idea del contenido de cada una.

+ Clasifique los tipos de datos para ayudarme en el EDA.

+ calcule la mediana, la moda, la media y los quartiles.

+ Realice una visualizacion de los cuartiles la media y los outliers por m,edio de un grafico de cajas, con ayuda de la libreria matplotlib.

+ Cree una nueva columna en el dataframe Hosp_train que clasificaba a los hospitalizados con 8 dias o mas y los que tenian menos de 8 dias hospitalizados.

+ Visualice la nueva columna para verificar que todo este bien.

+ Visualice la correlacion entre esta nueva columna y los datos categoricos de los dataframe, por medio de graficos de correlacion lineal, con ayuda de matplotlib.

+ Realice un analisis basado en mi interpretacion de los datos y los graficos previamente hechos, para descartar las columnas que no me servirian para mi modelo de ML.

+ Elimine las columnas ya mencionadas.

+ Algunas de las columnas con datos categoricos me dieron dudas de si era necesario tenerlas asique cree creé un filtro con los pacientes con una estadia mayor a 8 dias, sumé los datos unicos de cada columna categorica con este filtro y lo compare a las suma de todos los datos, sin el filtro.

+ Elimine las columnas que con esta comparacion interprete como innecesarias para mi modelo de ML.

+ Lleve a cavo un One Hot Encoder con ayuda de la funcion .get_dummies de pandas, para todas las columnas categoricas que quedaban, creando asi 2 nuevos dataframes.

+ Elimine la columna 'Stay (in days)' del dataframe creado previamente.

**Modelo**

Contodo el analisis exploratorio considere que el modelo que debia hacer era un arbol de desiciones, asique prcedi a crearlo y entrenarlo:

+ cree dos nuevos dataframes a partir del dataframe de entrenamiento 'OneHot_Hosp_train'. Uno sin la columna 'stay' y otro unicaente con la columna 'stay'

+ utilice la funcion de sklearn train_test_split para crear x de entrenamiento y de testeo con estos nuevos data frames, dividiendo la data 70-30 respectivamente.

+ entrene el modelo

+ vizualice el modelo

+ Probe el modelo con los x e y de testeto creados previamente.

+ Calcule el accurancy, el recall y la matriz de confusion.

+ Por ultimo lleve a cabo una ultima prediccion con el dataframe 'OneHot_Hosp_test' y exporte el resultado en un csv llamado 'MarEluneyGomez.csv'
