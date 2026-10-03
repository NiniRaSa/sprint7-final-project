README — Análisis de Clientes y Patrones de Uso — ConnectaTel
📊 Análisis de Clientes y Patrones de Uso — ConnectaTel    
📌 Descripción del proyecto
En este proyecto se analiza cómo utilizan los servicios los clientes de ConnectaTel.
El objetivo es conocer mejor a los clientes, encontrar patrones de uso, agruparlos según sus características y encontrar oportunidades para mejorar los planes y ofertas de la empresa.
Para realizar el análisis se utilizaron Python y diferentes herramientas para limpiar, analizar y mostrar los datos.
🎯 Objetivos
Los principales objetivos del proyecto son:
•	Conocer y entender los datos disponibles.
•	Encontrar y corregir errores en los datos.
•	Revisar datos faltantes, valores incorrectos y fechas que no son válidas.
•	Crear medidas que permitan conocer el comportamiento de cada cliente.
•	Agrupar a los clientes según su edad y nivel de uso.
•	Detectar valores muy altos o muy bajos en el consumo.
•	Proponer ideas que puedan ayudar a mejorar las ofertas de la empresa.

🗂️ Datos utilizados
Para realizar el análisis se utilizaron tres archivos principales:
•	plans.csv: los planes actuales (precio, minutos incluidos, GB incluidos, costo por extra).
•	users_latam.csv: información de clientes: edad, ciudad, fecha de registro, plan contratado.
•	usage.csv: el detalle de uso real: llamadas (duración) y mensajes (longitud).

Algunas de las variables utilizadas fueron:
•	user_id
•	age
•	city
•	plan
•	type
•	duration
•	length
•	date
🛠️ Herramientas utilizadas
•	Python: lenguaje utilizado para realizar el análisis.
•	Pandas: para organizar, limpiar y analizar los datos.
•	NumPy: para realizar operaciones con los datos.
•	Seaborn: para crear gráficos.
•	Matplotlib: para crear y personalizar gráficos.
•	Jupyter Notebook: para desarrollar y documentar el análisis.
•	GitHub: para guardar y compartir el proyecto.
🧹 Limpieza de los datos
Durante la revisión de los datos se encontraron algunos problemas:
•	El valor -999 aparecía en la variable age.
•	El símbolo ? aparecía en la variable city.
•	Había fechas futuras, correspondientes al año 2026, en reg_date.
•	Había valores vacíos en las variables duration y length.
Para solucionar estos problemas:
•	Los valores -999 en la edad fueron reemplazados utilizando la mediana de las edades válidas.
•	Los valores ? en la ciudad fueron tratados como datos faltantes.
•	Las fechas futuras fueron identificadas y cambiadas a valores nulos.
Valores vacíos que son normales
También se encontró que algunas columnas tienen muchos valores vacíos dependiendo del tipo de evento.
Por ejemplo:
•	duration tiene aproximadamente 99.93% de valores vacíos en los mensajes, porque un mensaje no tiene duración de llamada.
•	length tiene aproximadamente 99.93% de valores vacíos en las llamadas, porque una llamada no tiene longitud de mensaje.
Estos valores no se consideraron errores. Se mantuvieron vacíos porque esa información no aplica al tipo de evento.
👥 Segmentación de clientes
Para conocer mejor a los clientes, se crearon grupos según su edad y nivel de uso.
Segmentación por edad
•	Joven: menores de 30 años.
•	Adulto: entre 30 y 59 años.
•	Adulto mayor: 60 años o más.
Segmentación por nivel de uso
•	Bajo uso: menos de 5 llamadas y menos de 5 mensajes.
•	Uso medio: menos de 10 llamadas y menos de 10 mensajes.
•	Alto uso: clientes que no cumplen las condiciones anteriores.
Esta clasificación permite comparar diferentes tipos de clientes y entender mejor cómo utilizan los servicios.
📈 Análisis de los datos
Durante el análisis se crearon diferentes gráficos para observar:
•	La distribución de las edades.
•	La cantidad de mensajes enviados.
•	La cantidad de llamadas realizadas.
•	Los minutos utilizados en llamadas.
•	La cantidad de clientes según su nivel de uso.
•	La cantidad de clientes según su grupo de edad.
•	Los valores muy altos o muy bajos mediante gráficos de caja (boxplots).
🔎 Principales resultados
El análisis mostró que los clientes tienen diferentes niveles de consumo.
Al separar a los clientes por edad y nivel de uso, es posible identificar diferentes perfiles y entender mejor sus hábitos.
También se encontraron algunos valores de consumo muy altos o muy bajos. Estos valores no deben eliminarse automáticamente, ya que pueden corresponder a clientes reales que utilizan mucho más el servicio que otros.
Además, se encontraron valores vacíos en duration y length que están relacionados con el tipo de evento. Estos valores son normales porque no todos los datos aplican a todos los tipos de eventos.
💡 Recomendaciones
A partir del análisis se proponen las siguientes ideas:
•	Crear ofertas diferentes según el nivel de consumo de cada cliente.
•	Considerar beneficios adicionales para los clientes que tienen un consumo alto.
•	Combinar la edad y el nivel de uso para crear grupos de clientes más específicos.
•	Revisar los casos de consumo muy alto para saber si corresponden a clientes con necesidades especiales o a posibles errores en los datos.
•	Mejorar la forma en que se recopilan y validan los datos para reducir errores.
•	Realizar este tipo de análisis periódicamente para detectar cambios en el comportamiento de los clientes.
📁 Estructura del proyecto
connectatel-data-analysis/
├README.md
├connectatel_analysis.ipynb
 └── data/
    ├ plans.csv
    ├users_latam.csv
     └ usage.csv
•	Nota: los archivos de datos pueden omitirse del repositorio si contienen información sensible o si las condiciones del curso no permiten compartirlos.
🚀 Cómo ejecutar el proyecto
1.	Descargar o clonar este repositorio.
2.	Abrir el archivo connectatel_analysis.ipynb en Jupyter Notebook o JupyterLab.
3.	Instalar las librerías necesarias:
pip install pandas numpy seaborn matplotlib
4.	Ejecutar las celdas del notebook en orden.
👩‍💻 Autora
Nini Ramirez
Proyecto realizado como parte de mi formación en Data Analytics.
En este proyecto trabajé en diferentes etapas del análisis de datos, incluyendo la limpieza de datos, el análisis exploratorio, la segmentación de clientes y la búsqueda de información que pueda ayudar a tomar mejores decisiones para una empresa.


•	Herramientas y librerías principales.
•	Etapas del análisis.
•	3–5 hallazgos principales con cifras concretas.
•	Recomendaciones de negocio derivadas del análisis.
•	Instrucciones para ejecutar el notebook.
•	Estructura del repositorio y descripción de los archivos principales.
