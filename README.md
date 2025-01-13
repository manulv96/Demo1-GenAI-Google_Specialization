# <h1 align=center>**`Data Science - Demo 1 GenAI Flipkart ecommerce`**</h1>

En este repositorio podrán observar el contenido de los archivos utilizados para el desarrollo de la CLoud Function para el agente ***Corebi_demo_1***.

## **Pasos del proceso**

1. Se crean un archivo python **function-source/configs.py** para definir las variables de entorno para la cloud function.

2. Se crea un archivo python **function-source/prompts.py** con todos los prompts necesarios para el agente, que se encargaran de procesar las preguntas y responder al usuario. Junto con una consulta en lenguaje SQL en donde se obtienen las columnas de la tabla.

3. El archivo **function-source/utils_bq.py** contiene una función que ejecuta una consulta SQL y otra función que se encarga de obtener la pregunta del usuario y responder utilizando una LLM.

4. El archvio **function-source/utils_ds.py** contiene una función que se encarga de buscar los productos en el datastore segpun la consulta del usuario, a traves de un motor de busqueda que hace una busqueda de vectores en los emmbedings del datastore. 

5. El archivo **function-source/main.py** contiene la función para e dialogflow webhook donde llama a las funciones utils_ds.py y utils_bq.py segun corresponda luego de iniciar un chat utlizando el modelo Gemini de Google, y se encarga de responder las preguntas del usuario con la información proporcionada por estas funciones. 

## **Aclaraciones**

+ **function-source/requirements.txt:** define las dependencias necesarias para ejecutar correctamente el archivo main.py.


## Code origin certification

Todos los códigos utilizados fuero desarrollados por CoreBI S.A..


Todos los componentes utilizados son open source.
