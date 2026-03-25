# 🛋️ DECO.AI - Interiorista Personal Impulsado por IA

---

## Presentación de la Start-up

Bienvenidos al repositorio oficial de **DECO.AI**, el mini-proyecto final para la asignatura "Deep Learning", del Máster en Ciencia de Datos ETSE-UV.

**DECO.AI** es una plataforma de diseño de interiores accesible que utiliza modelos de Inteligencia Artificial pre-entrenados para transformar cualquier espacio al instante. Nuestra solución aborda el problema del alto coste y la dificultad de imaginar una remodelación.

### ¿Cómo funciona?

1.  **Sube tu foto:** El usuario proporciona una imagen real de su habitación actual.
2.  **Describe tu idea:** Introduce texto indicando el estilo buscado (ej: "Estilo nórdico minimalista y luminoso").
3.  **La IA actúa:** Nuestra plataforma analiza el espacio, propone un diseño remodelado respetando la estructura original y genera una lista de la compra.

---

## 📸 Ejemplos de Transformación

A continuación, mostramos algunos resultados obtenidos con nuestro motor estable:

| Habitación Original (Antes) | Resultado Remodelado (Después) |
|---|---|
| ![Antes](imagenes/foto_antes1.jpg) | ![Después](imagenes/foto_despues1.jpg) |
| *Comentario: Ejemplo de transformación de salón * | |

---

## 🛠️ Arquitectura Técnica y Organización del Repositorio

El proyecto se ha desarrollado siguiendo un enfoque modular, probando cada componente por separado antes de unificarlo. Todos los notebooks están diseñados para ejecutarse en **Google Colab con aceleración por GPU (T4)**.

Necesitarás una **API Key de Gemini** configurada como secreto en Colab con el nombre `clave_API_gemini` para los notebooks que usan el LLM.

### 📚 Desarrollo Modular (Paso a Paso)

Estos cuadernos contienen las pruebas independientes de cada módulo:

1.  **`1_Analisis_Estilo.ipynb`**: **Módulo Cerebro**. Utiliza el modelo multimodal Gemini-2.5-Flash para analizar la foto original, extraer el estilo actual y generar una recomendación basada en la petición del usuario.
2.  **`2_Generacion_Imagen.ipynb`**: **Módulo Artístico**. Utiliza ControlNet (Canny Edge) combinado con Stable Diffusion v1.5 para generar la imagen remodelada respetando estrictamente la geometría de la habitación.
3.  **`3_Busqueda_Productos.ipynb`**: **Módulo Negocio**. Utiliza Gemini para extraer muebles clave del análisis y genera enlaces dinámicos de búsqueda real a tiendas como IKEA, Amazon o Zara Home.
4.  **`4_Motor_interactivo.ipynb`**: **Diseño Web**. Implementa una interfaz estilo web interactiva usando Gradio, permitiendo al usuario introducir sus imágenes y peticiones de forma intuitiva y agradable a la vista.

### 🏆 Notebooks Finales (Unificados)

* **`DecoAI.ipynb`**: **[RECOMENDADO]**. Versión estable que integra perfectamente los notebooks 1, 2, 3 y 4. El Director de la Agencia IA propone 3 vías de diseño distintas y genera un pipeline completo de análisis, imagen y links de compra para cada una.

### 🧪 Versión Experimental

* **`DecoAI_2.0.ipynb`**: Este notebook añade una funcionalidad avanzada de **Inpainting (Pincel)**. Permite al usuario "pintar" con un pincel sobre la imagen original (ej: cambiar solo un sofá o una silla) y pedirle a la IA que cambie solo esa parte, manteniendo el resto de la habitación idéntico.
    * *Nota: Esta funcionalidad es experimental y los resultados, aunque funcionales, están en fase de mejora.*

---

## 👥 Autores

Proyecto realizado por parejas para Aprendizaje Profundo:

* Pol Reig i Gómez (github.com/polreig)
* Pablo Carbonell Martínez (github.com/pacarma4)

---

## DecoAI Y DecoAI_pro
Fusiona el modo automático y el manual en pestañas de una misma web. Introduce la traducción silenciosa (el usuario escribe en español y la IA lo pasa a inglés para el render) y un algoritmo que ordena automáticamente la lista de la compra del producto más barato al más caro.

## DecoAI_V2.0
La evolución definitiva. Añade una tercera pestaña ("Mover Mueble") que permite al usuario dibujar una caja de origen y otra de destino para arrancar un mueble de su sitio, reconstruir la pared de fondo y colocar el mueble nuevo en otra parte de la habitación con perspectiva correcta.
