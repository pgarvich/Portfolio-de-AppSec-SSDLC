# Restful Booker – API Security & QA Testing

## Descripción
Este repositorio/documento presenta un ejercicio integral de **QA Manual y Testing de Seguridad sobre APIs REST**, utilizando la API pública **Restful Booker** como entorno de práctica.
El objetivo del proyecto es demostrar la capacidad de **diseñar, ejecutar y documentar pruebas de seguridad** con criterio profesional, utilizando herramientas estándar de la industria y alineándose a buenas prácticas OWASP.

---

🚀 Quick Wins del Proyecto:

Ejecución de 9 casos de prueba de seguridad complejos.

Reporte de 2 vulnerabilidades de severidad ALTA con sugerencias de mitigación técnica.

Uso de scripting en Postman para automatizar la comparación de longitudes de respuesta y tiempos.

## 📂 Contenido del Repositorio

- 📄 **Informe de Testing**  
  Documento principal con:
  - Casos de prueba detallados
  - Precondiciones y setup de datos
  - Resultados esperados vs obtenidos
  - Evidencias
  - Recomendaciones de mitigación

- 🐞 **Bug Reports**  
  Reportes de defectos asociados a vulnerabilidades detectadas (XSS / HTML Injection), incluyendo severidad, impacto y sugerencias técnicas.

- 📦 **Postman Collection**  
  Colección exportada con todos los requests y scripts utilizados para reproducir las pruebas.

---

## Objetivos del Proyecto
- Diseñar una **suite de pruebas de seguridad** sobre una API REST.
- Identificar vulnerabilidades comunes como SQL Injection, XSS y fallas de control de acceso.
- Validar el comportamiento del backend frente a entradas maliciosas.
- Documentar los resultados con enfoque QA: casos de prueba, evidencias, defectos y mitigaciones.

---

## Alcance de las Pruebas
Las pruebas se realizaron exclusivamente sobre los siguientes ejes:

### 🔐 SQL Injection
- Error-Based SQL Injection (GET y POST)
- Boolean-Based SQL Injection (GET y POST)
- Time-Based SQL Injection (POST body)

### 🧼 Validación de Entradas y Codificación de Salidas
- HTML Injection
- Stored XSS / Tag Injection

### 🚪 Control de Acceso
- Acceso a recursos protegidos sin autenticación
- Acceso con token inválido

> Nota: La API utilizada es un entorno de práctica. Los hallazgos se analizan desde una perspectiva educativa y profesional.

No se realizaron pruebas de fuerza bruta, DoS, fuzzing ni escaneo automatizado.

---

## Metodología
- Testing manual orientado a riesgos.
- Enfoque black-box.
- Requests ejecutados con **Postman**.
- Comparación de respuestas por:
  - Status code
  - Estructura del body
  - Longitud de respuesta
  - Tiempos de respuesta
- Evidencias recolectadas por request.

---

## Entorno de Pruebas
- API: https://restful-booker.herokuapp.com
- Herramienta: Postman
- Formato de intercambio: JSON
- Autenticación: Token-based / Basic Auth (según endpoint)

---

## Resultados Generales
- **SQL Injection**: No se detectaron vulnerabilidades explotables.
- **Access Control**: Implementación correcta de controles de autenticación.
- **Input / Output Validation**: Se detectaron fallas que permiten almacenar y devolver contenido HTML/JS sin escape.

Las fallas de sanitización representan un **riesgo potencial para aplicaciones cliente** que rendericen los datos sin controles adicionales.

---

## Valor del Ejercicio
Este proyecto demuestra:
- Capacidad de análisis más allá del uso de herramientas automáticas.
- Comprensión de por qué una prueba es relevante (o no) en una API.
- Criterio para evitar pruebas redundantes y reportes inflados.
- Documentación clara, estructurada y orientada a equipos técnicos.

---

## 🧠 Criterio de Testing

El proyecto prioriza:
- Reproducibilidad de las pruebas
- Evitar falsos positivos
- Uso de distintos vectores de ataque para un mismo endpoint
- Documentación clara orientada a equipos técnicos y de negocio

---
## Nota Importante
Restful Booker es un entorno de práctica deliberadamente simple. Las vulnerabilidades detectadas no deben interpretarse como fallas de un sistema productivo real, sino como parte del aprendizaje y demostración técnica.

---

## Autor
Ejercicio realizado como práctica profesional de QA Manual y Security Testing.
