# Portfolio de AppSec & SSDLC

## De la teoría a la validación práctica

Este repositorio documenta mi proceso de formación y aplicación de controles de **Seguridad de Aplicaciones (AppSec)** a lo largo de un **Ciclo de Vida de Desarrollo de Software Seguro (SSDLC)**.

El proyecto combina **diseño preventivo (Shift-Left)**, **análisis automatizado (SAST/DAST)** y **testing manual**, con foco en **criterio técnico, validación práctica y remediación**, más allá del uso mecánico de herramientas.

---

## 🚀 Propósito del proyecto

Demostrar la capacidad de **analizar, detectar, validar y priorizar vulnerabilidades** utilizando estándares de la industria (OWASP, CWE, ASVS) y herramientas reales, aplicando análisis contextual para reducir falsos positivos y generar hallazgos accionables para equipos de desarrollo.

---

## 📂 Alcance y estructura del portfolio

El portfolio se organiza en **tres pilares**, alineados al ciclo completo de seguridad:

---

### 1️⃣ Planificación y diseño seguro (Shift-Left)

Aplicado sobre una **aplicación hipotética de gestión para PYMEs**.

**Actividades principales**

* Modelado de amenazas utilizando **STRIDE** (OWASP Threat Dragon).
* Identificación de activos críticos, actores y vectores de ataque.
* Definición de **requisitos de seguridad** alineados con **OWASP ASVS** y **OWASP Proactive Controls**.

**Artefactos generados**

* Documentos de contexto y alcance.
* Diagramas de flujo de datos (DFD).
* Matriz de riesgos y priorización.

---

### 2️⃣ Implementación práctica de SSDLC (SAST & DAST)

Aplicado sobre una **Web App monolítica desarrollada en Django** (Buscador Rick & Morty).

**Análisis estático (SAST)**

* Ejecución y triaje de hallazgos con **SonarCloud** y **Semgrep**.
* Identificación de vulnerabilidades reales (por ejemplo, **exposición de `SECRET_KEY`**).
* Análisis contextual y descarte de **falsos positivos**.

**Análisis dinámico (DAST)**

* Escaneo e interceptación de tráfico con **Burp Suite Professional**.
* Validación de controles de seguridad en tiempo de ejecución.

**Correlación SAST / DAST**

* Verificación manual de hallazgos de código en el comportamiento real de la aplicación.
* Ejemplo: comprobación efectiva de protecciones **CSRF** y controles de acceso.

---

### 3️⃣ API Security & QA Testing

Testing manual orientado a riesgos sobre la API **Restful Booker**.

**Vectores de ataque evaluados**

* SQL Injection (Error-based, Boolean-based, Time-based).
* Inyección HTML y XSS.
* Fallos de control de acceso y validación de lógica.

**Herramientas y técnicas**

* Testing manual y automatización de validaciones con **Postman**.

**Entregables**

* Bug Reports detallados con:

  * Descripción técnica.
  * Severidad e impacto.
  * Evidencia.
  * Recomendaciones de mitigación.

---

## 🛠️ Stack tecnológico

**Análisis y seguridad**

* Burp Suite Professional
* SonarCloud
* Semgrep
* OWASP Threat Dragon

**Testing y desarrollo**

* Postman (API Testing)
* Python / Django

**Frameworks y estándares**

* OWASP Top 10
* OWASP ASVS
* STRIDE
* CWE

---

## 🧠 Criterio y metodología

Este proyecto prioriza:

* **Reducción de falsos positivos**: no todo hallazgo automático representa una vulnerabilidad explotable.
* **Validación práctica**: cada finding relevante se intenta reproducir manualmente.
* **Trazabilidad**: correlación entre código, ejecución y reporte.
* **Orientación a remediación**: cada vulnerabilidad incluye sugerencias técnicas claras para el equipo de desarrollo.

---

## 📈 Próximos pasos

Este repositorio se encuentra en evolución. Próximas iteraciones incluyen:

* **Análisis de Logs y Monitoreo**: Integrar la aplicación en un entorno de visibilidad (SIEM) para analizar los logs generados durante la fase de DAST.
* **Detección de Intrusiones**: Desarrollar reglas de detección (Sigma/YARA) basadas en los vectores de ataque identificados en el modelado de amenazas.
* **Hardening de Infraestructura**: Aplicar configuraciones de seguridad a nivel servidor (Nginx/WAF) para mitigar las vulnerabilidades halladas en la fase dinámica.

---

## 👤 Perfil objetivo
Este proyecto demuestra competencias analíticas aplicables a roles de:

* **Analista de SOC L1 / L2**: Capacidad de entender ataques web y diferenciar tráfico legítimo de malicioso.
* **Blue Teamer**: Enfoque en la identificación de vulnerabilidades para la creación de estrategias de defensa.
* **Analista de Seguridad**: Visión integral del ciclo de vida de un incidente, desde la vulnerabilidad hasta el reporte técnico.

**Pedro Garvich**
LinkedIn: [https://linkedin.com/in/pgarvich](https://linkedin.com/in/pgarvich)
Email: [pgarvich@gmail.com](mailto:pgarvich@gmail.com)
