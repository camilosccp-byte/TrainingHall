# TrainingHall
There I decided to provide a new an unusual tool providing remarkable insights in a training scope for clubs (and why not national soccer teams), I used eventing data and some historical data to create a powerful training for tactical and technical skills

# ⚽ Recomendador de Entrenamientos - Piloto Liga

Este es un prototipo funcional de una aplicación web interactiva desarrollada en **R Shiny**. Su objetivo es optimizar la toma de decisiones en cuerpos técnicos mediante la recomendación automatizada de sesiones de entrenamiento. 

La app compara el rendimiento de un jugador con los promedios estandarizados de la liga en dos posiciones clave: **Delantero Centro** y **Volante Mixto**.

## 🚀 Características Principales

- **Datos Dinámicos de Liga:** Conexión automatizada con la API de **StatsBomb** para extraer métricas reales de partidos y calcular las medias de rendimiento de la liga.
- **Scraping de Metodologías:** Extracción de ejercicios de entrenamiento actualizados mediante técnicas de Web Scraping (`rvest`).
- **Filtrado Condicional:** Interfaz de usuario inteligente que adapta los formularios de ingreso de datos según la posición seleccionada.
- **Alertas Automatizadas:** Sistema de sugerencias que prioriza los entrenamientos si el jugador se encuentra por debajo del umbral promedio.

## 📊 Métricas Evaluadas por Posición

Como fase piloto, la aplicación evalúa un límite de 2 métricas y 2 entrenamientos por rol:

| Posición | Métricas Extraídas (StatsBomb) | Entrenamientos Disponibles (Scraping) |
| :--- | :--- | :--- |
| **Delantero Centro** | Goles por partido / Remates a puerta | Circuito de Definición / Ataque Espacios Reducidos |
| **Volante Mixto** | Pases clave / Intercepciones por partido | Transición Alta Intensidad / Presión Tras Pérdida |

## 🛠️ Requisitos e Instalación

Para ejecutar este proyecto localmente, necesitas tener instalado **R** y **RStudio**.

1. Clona este repositorio en tu computadora:
   ```bash
   git clone https://github.com/camilosccp-byte/TrainingHall.git
   ```

2. Abre RStudio e instala los paquetes necesarios ejecutando el siguiente código en la consola:
   ```R
   install.packages(c("shiny", "bslib", "rvest", "tidyverse", "remotes"))
   remotes::install_github("statsbomb/StatsBombR")
   ```

3. Abre el archivo `Shiny App` y haz clic en el botón **"Run App"** (o ejecuta `shiny::runApp()`).

## 📁 Estructura del Proyecto

- `Shiny App`: Archivo principal que contiene la interfaz de usuario (UI), la lógica del servidor (Server) y las funciones de extracción de datos.
- `README.md`: Documentación del proyecto (este archivo).

## 📝 Próximas Mejoras (Roadmap)
- [ ] Implementar un sistema de caché (`.RData`) para evitar consultas repetitivas a StatsBomb en cada inicio.
- [ ] Expandir el catálogo a más de 2 entrenamientos por posición utilizando bases de datos relacionales.
- [ ] Incluir reportes descargables en formato PDF para los entrenadores.
