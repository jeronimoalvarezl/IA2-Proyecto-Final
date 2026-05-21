# Sports Analytics using Deep Learning Models

## Descripción

Este proyecto entrena un modelo de detección de objetos utilizando YOLOv8 y transfer learning para detectar jugadores de fútbol y la pelota en un video capturado desde una perspectiva aérea.

Además, el modelo genera visual analytics por frame, como el conteo de jugadores en cada lado de la cancha, jugadores fuera del campo, jugadores dentro de las áreas penales y la ubicación aproximada de la pelota.

## Videos

Como los videos son de más de 100mb no se pueden subir a GitHub, dejamos los links de drive para su descarga aquí:

Video Original: https://drive.google.com/file/d/1fXZQ55r1Rt3BeeL3xxW0cIyyNAex-8Ze/view?usp=sharing
Video Resultados: https://drive.google.com/file/d/15rxMLx5fssmA2qkycdhJvCKOZJa6ld3D/view?usp=sharing

## Requisitos

Instalar las siguientes librerías de Python:

```
ultralytics
roboflow
opencv-python
moviepy
ipython
matplotlib
numpy
pandas
torch
torchvision
```

## Ejecutar el notebook

1. Clonar el repositorio:

```
git clone https://github.com/antoniorivag/IA2-Proyecto-Final.git
cd IA2-Proyecto-Final
```

2. Asegurarse de tener el video original y el dataset configurado correctamente.

3. Instalar las librerías necesarias:

```
pip install -r requirements.txt
```

4. Ejecutar todas las celdas del notebook en orden.

5. Al finalizar, se genera un video de salida con las detecciones y visual analytics:

```
VisualAnalytics.mp4
```

## Dataset

El dataset fue creado a partir del video proporcionado para el proyecto.

Se etiquetaron manualmente 580 frames usando Roboflow, con las siguientes clases:

- Jugador
- Pelota

El dataset fue exportado en formato YOLOv8 y dividido en:

- 70% entrenamiento
- 15% validación
- 15% prueba

## Modelo

Se utilizó YOLOv8m como modelo base, aplicando transfer learning con el dataset personalizado.

Principales parámetros de entrenamiento:

- Épocas: 100
- Tamaño de imagen: 1280
- Batch size: 4
- Patience: 15

## Autores

Antonio Rivera, Jerónimo Alvarez
