Alumnos: Olivia Troitiño Frydrych y Claudia Gascó Miranda

# Práctica 3 - Análisis de Grafos: Red de Personajes Marvel

## Descripción
Este proyecto tiene como objetivo construir un grafo basado en cómics y personajes de Marvel, donde cada personaje será un nodo y los enlaces entre ellos se crean si aparecen en el mismo cómic.




## Estado Actual
⚠️ **Problema con la API de Marvel**

El proyecto actualmente no puede acceder a la API de Marvel debido a un error de autenticación. Se están recibiendo los siguientes errores:

```
Status code: 418
Response: {"code":"ImATeapotError","message":"I am a teapot: Error: Server not available"}
```

### Posibles causas del error:
1. Problemas de autenticación con las claves API
2. Posible expiración de las claves API
3. Límite de solicitudes excedido
4. Problemas temporales con los servidores de Marvel
### Soluciones intentadas:
- Generación correcta del hash 
- Verificación de las claves API
- Pruebas con diferentes endpoints
- Añadir headers de navegador
- Uso de timestamp fijo y dinámico

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

## Datos y Análisis
A pesar del problema actual con la API, contamos con:
1. Un archivo CSV (`marvel_characters.csv`) que contiene datos extraídos previamente cuando la API funcionaba correctamente
2. Un análisis completo en `analisis.ipynb` que incluye:
   - Construcción del grafo
   - Análisis de centralidad
   - Visualización de la red
   - Estadísticas de los personajes y sus conexiones

## Requisitos
- Python 3.x
- Bibliotecas:
  - requests
  - pandas
  - python-dotenv
  - networkx
  - matplotlib

## Configuración
El archivo `.env` debe contener:
```
PUBLIC_KEY=tu_public_key
PRIVATE_KEY=tu_private_key
HASH=tu_hash
```

## Nota
Este proyecto está actualmente en pausa en cuanto a la extracción de nuevos datos de la API de Marvel. Sin embargo, el análisis completo ya está realizado y disponible en `analisis.ipynb`.
