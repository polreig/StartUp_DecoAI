# StartUp_DecoAI
Proyecto de inteligencia artificial para diseño de interiores, con generación de imágenes, análisis de espacios y tienda interactiva. Materiales + Multi-tienda.
## 1_Análisis_Estilo
El archivo actúa como un diseñador de interiores virtual. Implementa a Gemini para analizar una foto y la petición del usuario, devolviendo el estilo actual, una recomendación de nuevo estilo, elementos clave y una paleta de colores.
## 2_Generación_Imagenes
Es el primer prototipo de IA generativa. Integra Stable Diffusion con ControlNet (Canny Edge) para extraer las líneas de la habitación (la estructura) y generar un nuevo diseño fotorrealista que respete la perspectiva original.

## Noteboof_final
Archivo intermedio que fusiona estos tres primeros pasos en un pipeline completo. El motor_deco_ai recibe la foto, la petición y las medidas, y devuelve el análisis de estilo, la imagen con el nuevo diseño y una tienda interactiva con enlaces afiliados a los productos recomendados. Es el núcleo de DecoAI, el "cerebro" que procesa toda la información y genera resultados personalizados para cada usuario.

## Notebook_final_pro
El Motor Universal "Pro". Revoluciona la detección usando Mask2Former para reconocer automáticamente superficies (suelos, paredes) y objetos sin que el usuario pinte. Además, mejora el carrito de la compra añadiendo enrutamiento inteligente a tiendas como Leroy Merlin, Bauhaus, Zara Home y Maisons du Monde.

## 4_Motor_interactivo
Introduce Gradio para crear una aplicación web real. Pasa de un modelo automático a uno donde el usuario puede usar un "pincel" para pintar sobre el mueble exacto que quiere cambiar, rellenando solo esa zona con Inpainting y estructurando con MLSD.

## DecoAI Y DecoAI_pro
Fusiona el modo automático y el manual en pestañas de una misma web. Introduce la traducción silenciosa (el usuario escribe en español y la IA lo pasa a inglés para el render) y un algoritmo que ordena automáticamente la lista de la compra del producto más barato al más caro.

## DecoAI_V2.0
La evolución definitiva. Añade una tercera pestaña ("Mover Mueble") que permite al usuario dibujar una caja de origen y otra de destino para arrancar un mueble de su sitio, reconstruir la pared de fondo y colocar el mueble nuevo en otra parte de la habitación con perspectiva correcta.