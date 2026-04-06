# MockAPI CRUD Testing

Colección de pruebas CRUD en Postman sobre una API REST construida con MockAPI. Cubre casos positivos, negativos y restablecimiento de datos entre ejecuciones.

## Herramientas

- [Postman](https://www.postman.com/)
- [MockAPI](https://mockapi.io/)

## Estructura de la colección

| Carpeta | Descripción |
|---|---|
| Tests Positivos | Casos happy-path para GET, POST, PUT y DELETE |
| Tests Negativos | Casos de borde: IDs inválidos, body vacío, campos no definidos, URL incorrecta |
| Restablecer | Requests de limpieza que restauran el estado de la API entre ejecuciones |

## Cómo importar

1. Clonar o descargar el repositorio
2. Abrir Postman
3. Ir a **Import** y seleccionar el archivo `.json`
4. Configurar la variable `base_url` con el endpoint de la API

## Hallazgos documentados

Algunos tests negativos fallan intencionalmente. MockAPI es una API permisiva que acepta bodies vacíos y campos no definidos retornando `201`. Estos casos están documentados como defectos de diseño de la plataforma, no errores de los tests.

## Cobertura

- 16 requests en total
- 12 assertions
- Validación de código de estado y contenido de respuesta
