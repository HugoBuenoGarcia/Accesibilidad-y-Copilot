# Accessibility Refactoring with AI / Refactorización de Accesibilidad con IA

## 🇬🇧 English Description

### Project Overview
This repository demonstrates the process of transforming non-accessible HTML code into WCAG 2.2 compliant code (Level AA/AAA) using AI-assisted programming (GitHub Copilot / Gemini).

### Methodology
1.  **Original State:** Several HTML files were created with intentional accessibility errors (missing labels, `div` buttons, poor contrast, missing semantics).
2.  **Prompt Engineering:** A specific prompt was designed to guide the AI to apply WCAG 2.2 standards, prioritizing semantic HTML over ARIA where possible.
3.  **Validation:** The code was tested before and after using industry-standard tools.

### The "Perfect Prompt" Used
> *"Actúa como un Auditor Senior de Accesibilidad Web... [Insertar el prompt completo aquí]..."*

### Validation Tools
* **WAVE:** Used to visualize structural errors and contrast issues.
* **Lighthouse:** Used for overall accessibility scoring.
* **Axe DevTools:** Used for deep technical analysis.

### Results
* **Before:** The original code contained [X] errors and [Y] alerts.
* **After:** The refactored code achieved a score of 100% on Lighthouse and 0 Errors on WAVE.

---

## 🇪🇸 Descripción en Español

### Resumen del Proyecto
Este repositorio demuestra el proceso de transformación de código HTML no accesible a código compatible con WCAG 2.2 (Nivel AA/AAA) utilizando asistentes de programación basados en IA.

### Metodología
1.  **Estado Original:** Se crearon archivos HTML con errores de accesibilidad intencionados (falta de etiquetas, botones hechos con `div`, bajo contraste, falta de semántica).
2.  **Ingeniería de Prompts:** Se diseñó un prompt específico para guiar a la IA hacia los estándares WCAG 2.2, priorizando HTML semántico sobre ARIA siempre que fuera posible (siguiendo buenas prácticas como las de Olga Carreras).
3.  **Validación:** El código fue testeado antes y después usando herramientas estándar de la industria.

### El Prompt Utilizado
(Ver sección en inglés o el archivo `prompt.txt` incluido en este repo).

### Herramientas de Validación
* **WAVE (Web Accessibility Evaluation Tool):** Para visualizar errores estructurales y de contraste.
* **Lighthouse (Chrome):** Para puntuación general.
* **Axe DevTools:** Para análisis técnico profundo.

### Problemas Encontrados y Soluciones
1.  **Semántica:** La IA inicialmente sugirió `role="button"` en un `div`.
    * *Solución:* Se ajustó el prompt para forzar el uso de la etiqueta nativa `<button>`.
2.  **Contraste:** Los colores por defecto no pasaban el ratio 4.5:1.
    * *Solución:* El prompt instruyó a la IA para añadir CSS inline o sugerir clases con alto contraste.
3.  **Formularios:** Faltaban asociaciones `for/id`.
    * *Solución:* La IA reescribió todos los inputs envolviéndolos o vinculándolos con sus labels.

### Evidencia (Screenshots)
Las capturas de pantalla de los informes de WAVE y Lighthouse se encuentran en la carpeta `/reports`.

* [Ver Informe Antes](./reports/before-wave.png)
* [Ver Informe Después](./reports/after-wave.png)
