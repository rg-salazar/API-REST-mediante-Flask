# Despliegue Local de Modelo Predictivo con Flask y Docker


![Python](https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-F7931E?style=for-the-badge&logo=scikitlearn&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?style=for-the-badge&logo=docker&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white)

## Objetivo
Desarrollar un sistema completo que integre un modelo de Machine Learning (clasificación o regresión), exponerlo como API REST mediante Flask, y contenedorizado con Docker. Se espera demostrar buenas prácticas de versionado, empaquetado y documentación.

## Contexto
Este proyecto simula el despliegue de un modelo predictivo para una fintech o startup de salud, permitiendo integrar un modelo de predicción (por ejemplo, scoring de crédito o diagnóstico preventivo) dentro de su infraestructura tecnológica. El servicio desarrollado busca ser:

- Escalable localmente mediante contenedores
- Fácil de actualizar
- Accesible vía REST

## Tecnologías utilizadas
- **Python**: Lenguaje principal del proyecto  
- **Flask**: Framework para exponer el modelo como API REST  
- **Docker**: Contenerización del servicio  
- **scikit-learn / XGBoost**: Librerías de Machine Learning  
- **pytest**: Framework para pruebas automatizadas



## Instalación y ejecución local
1. **Clonar repositorio**

git clone <URL_DEL_REPOSITORIO>
cd project
Construir la imagen Docker


## Construcción y ejecución del contenedor

```bash
# 1. Construir la imagen Docker
docker build -t modelo-predictivo .

# 2. Ejecutar el contenedor
docker run -p 5000:5000 modelo-predictivo

# 3. Probar la API
# Endpoint de predicción: POST /predict
curl -X POST http://localhost:5000/predict \
-H "Content-Type: application/json" \
-d '{"feature1": 10, "feature2": 5, "feature3": 1}'

# 4. Testing
# Ejecuta pruebas automatizadas con:
pytest tests/

# Esto permite verificar que la API responde correctamente 
# y que el modelo predice según lo esperado.

# --- Buenas prácticas aplicadas ---
# - Versionado de código con Git
# - Contenerización para reproducibilidad
# - Documentación de endpoints y flujo de datos
# - Pruebas automatizadas para asegurar la estabilidad

# --- Futuras mejoras ---
# - Implementar autenticación para la API
# - Manejo de logs y métricas de uso
# - Integración con bases de datos para predicciones en lote

# --- Cómo cerrar la consola Bash ---
# Una vez finalizadas las pruebas, puedes cerrar la terminal Bash con:
exit
# o presionando:
# Ctrl + D

# Si estás ejecutando un contenedor Docker en modo interactivo, 
# 'exit' te sacará del contenedor, pero no lo detendrá.
# Para detenerlo completamente:
docker stop NOMBRE_DEL_CONTENEDOR

# Antes de cerrar, asegúrate de detener cualquier proceso activo (por ejemplo, un servidor Flask)
# presionando Ctrl + C
