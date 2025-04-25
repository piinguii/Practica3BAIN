Alumnos: Olivia Troitiño Frydrych y Claudia Gascó Miranda

# Práctica 3 - Análisis de Grafos: Red de Personajes Marvel

## Descripción
Este proyecto tiene como objetivo construir un grafo basado en cómics y personajes de Marvel, donde cada personaje será un nodo y los enlaces entre ellos se crean si aparecen en el mismo cómic.

## Imports necesarios
Este proyecto requiere las siguientes librerías para funcionar:
```
import requests
import pandas as pd
import time
import networkx as nx
import matplotlib.pyplot as plt
from networkx.algorithms import community
```
### Instalación de librerías
Si alguna de estas librerías no está instalada, puede instalarse utilizando los siguientes comandos:
```
pip install requests
pip install pandas
pip install networkx
pip install matplotlib
```
## Configuración
El archivo `.env` debe contener:
```
PUBLIC_KEY=tu_public_key
PRIVATE_KEY=tu_private_key
HASH=tu_hash
```

## Estado Actual
**Problema con la API**
El proyecto actualmente no puede acceder a la API de Marvel en el extractor debido a un error de autenticación. Cuando nos dejó de funcionar el extractor, probamos hacer lo siguiente:

### Soluciones intentadas:
- Verificación de las claves API
- Verificación del límite de llamadas a la API (Son 3000 por día, no habíamos hecho tantas este día.)
- Creación de nueva cuenta de Marvel Developer (Para verificar que no fuera un problema de la cuenta original, daba el mismo error que la cuenta original)
- Generación nueva del hash
- Pruebas con diferentes endpoints y reformateo de las requests (Otra vez más daba el mismo error.)

Este error sucedió el 25 de Abril al revisar el código una última vez antes de entregar la práctica, así que el resto de la práctica sigue funcionando con los datos obtenidos previamente.

```
Status code: 418
Response: {"code":"ImATeapotError","message":"I am a teapot: Error: Server not available"}
```

## Datos y Análisis
A pesar del problema actual con la API, contamos con:
1. Un archivo CSV (`marvel_characters.csv`) que contiene datos extraídos previamente cuando la API aún funcionaba correctamente
2. Un análisis en `analisis.ipynb` que incluye:
   - Construcción del grafo
   - Análisis de centralidad
   - Visualización de la red
   - Estadísticas de los personajes y sus conexiones

## Estructura del Proyecto
```
.
├── INPUT/
│   └── marvel_characters.csv (archivo con datos históricos de cuando la API funcionó)
├── grafo.gexf
├── README.md
├── extractor.ipynb
├── transformador.ipynb
└── analisis.ipynb
```
