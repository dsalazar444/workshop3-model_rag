# Workshop 3 — Asistente de Documentos con Gemini + Gradio

### Integrantes:

- Athina Cappelletti
- Daniela Salazar Amaya
- Laura Indabur 

Proyecto práctico para construir un chatbot que responde preguntas sobre un PDF (paper *Attention is All You Need*) usando Gemini, `pypdf` y Gradio.

## Contenido del proyecto

- [05_ejercicio.ipynb](05_ejercicio.ipynb): notebook guía (con consignas para completar).
- [05_ejercicio_solucion.ipynb](05_ejercicio_solucion.ipynb): notebook resuelto.

## Objetivo

Construir una app que:

1. Lea el contenido de un PDF.
2. Inyecte ese contenido en el contexto del modelo.
3. Responda **solo** con información del documento.

---

## Requisitos

- Python 3.10+
- API key de Gemini

Instala dependencias:

```bash
pip install pypdf gradio google-genai python-dotenv
```

## Configuración

Crea un archivo `.env` en la raíz del proyecto:

```env
GEMINI_API_KEY="tu_api_key_aqui"
```

Coloca el PDF en la carpeta del proyecto (por ejemplo `ia.pdf`, como en la solución).

## Cómo usar

1. Abre `05_ejercicio.ipynb` para realizar el ejercicio paso a paso.
2. Si quieres comparar o ejecutar directamente una versión completa, usa `05_ejercicio_solucion.ipynb`.
3. Ejecuta las celdas en orden.
4. Al lanzar Gradio, abre la URL local que aparezca en salida.

## Pruebas recomendadas

Haz preguntas sobre el contenido del paper, por ejemplo:

- ¿Cuál es la arquitectura principal propuesta?
- ¿Qué es el mecanismo de atención?
- ¿Cuántas capas tiene el encoder del modelo base?

Pregunta trampa sugerida:

- ¿Qué es GPT-4?

Comportamiento esperado: el asistente debe indicar que esa información no está en el documento, en vez de usar conocimiento externo.
