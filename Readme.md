# PyMetrics

Plataforma web local de análisis estadístico de inventario para PYMES del comercio minorista, con un asistente de interpretación basado en la API de Gemini.

**Stack:** HTML, CSS y JavaScript (Chart.js) · Python 3.10+ con FastAPI · SQLite · Excel (.xlsx) como entrada y salida · API de Gemini.

## Instalación (Windows)

```bash
cd pymetrics
python -m venv .venv
.venv\Scripts\activate
pip install -r requirements.txt
copy .env.example .env      # luego abra .env y pegue su GEMINI_API_KEY
```

En macOS o Linux use `source .venv/bin/activate` y `cp .env.example .env`.

La clave de Gemini se obtiene gratis en Google AI Studio (https://aistudio.google.com/apikey). Sin clave, la aplicación funciona igual, salvo el asistente de IA.

## Ejecución

```bash
uvicorn backend.app.main:app --reload
```

Abra **http://127.0.0.1:8000** y cargue `datos/inventario_ejemplo.xlsx` para probar.

# Pruebas

Para poder realizar las pruebas unitarias de este proyecto puedes usar este comando en la terminal.

```bash
python -m pytest -v
```


## Estructura

```
backend/
frontend/
datos/
tests/
.env.example.
.gitignore
Readme.md
requirements.txt
```

## Privacidad

A Gemini solo se envían indicadores agregados y códigos de producto. Nunca se envían los nombres ni el archivo original. En el nivel gratuito, Google puede usar el contenido enviado para mejorar sus productos, por lo que no deben incluirse datos sensibles.

## Integrantes
- Juan Jose Avendaño Zapata
- Samuel Stevan Arias tuquerres
- Oscar Julian castillo Zuñiga