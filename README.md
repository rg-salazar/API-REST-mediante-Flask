# Despliegue Local de Modelo Predictivo con Flask y Docker

## Objetivo
Desarrollar un sistema completo que integre un modelo de Machine Learning (clasificación o regresión), exponerlo como API REST mediante Flask, y contenedorizado con Docker. Se espera demostrar buenas prácticas de versionado, empaquetado y documentación, así como un flujo básico de pruebas automatizadas.

## Contexto
Este proyecto simula el despliegue de un modelo predictivo para una fintech o startup de salud, permitiendo integrar un modelo de predicción (por ejemplo, scoring de crédito o diagnóstico preventivo) dentro de su infraestructura tecnológica. El servicio desarrollado busca ser:

- Escalable localmente mediante contenedores
- Fácil de actualizar
- Accesible vía REST
- Documentado y probado con pruebas automatizadas

## Tecnologías utilizadas
- **Python**: Lenguaje principal del proyecto  
- **Flask**: Framework para exponer el modelo como API REST  
- **Docker**: Contenerización del servicio  
- **scikit-learn / XGBoost**: Librerías de Machine Learning  
- **pytest**: Framework para pruebas automatizadas



## Instalación y ejecución local
1. **Clonar repositorio**
```bash
git clone <URL_DEL_REPOSITORIO>
cd project

docker build -t modelo-predictivo .

docker run -p 5000:5000 modelo-predictivo

Probar la API

Endpoint de predicción: POST /predict

Ejemplo de request con curl:


## Estructura del proyecto
