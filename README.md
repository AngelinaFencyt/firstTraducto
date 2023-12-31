# Primer prototipo del proyecto interprete de lengua de señas!

Este proyecto tiene como objetivo procesar imágenes enviadas por usuarios a través de una API para hacer la predicción de que letra del abecedario de la lengua de seña esta haciendo en el momento de que envia la imagen. Estoy usando FastAPI, una biblioteca Python moderna y rápida para crear APIs, para crear nuestro servidor de procesamiento de imágenes.

# Empezamos

Esta es una API desarrollada con el fin de:

- Procesar imágenes enviadas por los usuarios en tiempo real.
- Hacer la predicción de que letra del abecedario de la lengua de seña esta haciendo en el momento de que envia la imagen.
- Devolver la predicción de la letra a los usuarios.

# Instalación

Primero como buena practica es crear un entorno virtual de desarrollo para este proyecto, para ello puedes usar el siguiente comando:

```python
python -m venv venv
```
Ahora que ya tienes el entorno virtual creado, puedes activarlo con el siguiente comando:

windows:
```python
venv\Scripts\activate
```
linux:
```python
source venv/bin/activate
```

Para comenzar simplemente debes clonar este repositorio y ejecutar el siguiente comando para instalar las dependencias necesarias para el proyecto

```
pip install -r requirements.txt --use-pep517

```

IMPORTANTE para la version de Python que se utilizo para este proyecto es la:

## Python 3.8 
(a dia de 04/02/2023 tiene errores con Python 3.11.1)
Por lo que se recomienda utilizar esta versión para evitar problemas con las dependencias aunque se puede trabajar con versiones anteriores o superiores si lo desea en excepción de la 3.6.0 y anteriores.

Ahora que ya tienes las dependencias instaladas, puedes ejecutar el siguiente comando para iniciar el servidor de desarrollo(Estando en la carpeta "app"):

```
uvicorn main:app --reload

```

y listo! ya tienes el servidor corriendo en [http://localhost:8000/docs](http://localhost:8000/docs) 🎉

# 🧱 Estructura

La estructura de la aplicación se divide en algunos componentes diferentes:

## 📁 app

Esta carpeta contiene el código de la aplicación. Aquí es donde se encuentra el código de la API y el código de procesamiento de imágenes.

## 📁 app/api

Esta carpeta contiene el código de la API. Aquí es donde se encuentra el código de FastAPI.

## 📁 app/api/endpoints

Esta carpeta contiene los endpoints de la API. Aquí es donde se encuentra el código de FastAPI para cada ruta.

## 📁 app/core

Esta carpeta contiene el archivo "artificial_intelligence_processor.py" que contiene el código para procesar las imágenes.

# Cómo funciona 

Cuando un usuario envía una imagen a través de una solicitud POST multipart/form-data al enpoint `/process-image`, la imagen se pasa al módulo processing_images.py, donde se procesa mediante MediaPipe. A continuación, hace la prediccion y estimacion y devuelve la letra a la que se puede estarse interpretando.


#Preguntas frecuentes

¿Qué es FastAPI? FastAPI es una biblioteca Python para crear APIs. Es moderno, rápido y fácil de usar.

¿Cómo procesa las imágenes? Usamos una combinación de bibliotecas de procesamiento de imágenes y código personalizado para procesar las imágenes enviadas por los usuarios con librerias como [mediapipe](https://mediapipe.dev/) y cálculos con numpy para hacer esta interpretación de señas.


# ¡Gracias por usar este interprete de señas!

Espero que disfrutes de este proyecto tanto como disfrute creándolo. ¡Haz algo genial con él!
# firstTraducto
# firstTraducto
