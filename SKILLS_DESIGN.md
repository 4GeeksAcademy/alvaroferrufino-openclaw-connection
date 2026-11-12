Este documento detalla el diseño conceptual, los inputs y los outputs esperados para las habilidades personalizadas (skills) implementadas de forma modular bajo la carpeta `skills-design/`.

---

## 1. `github-weekly-digest`

* **1. ¿Qué hace esta skill? (Una frase):** 
  Consolida y resume automáticamente el progreso técnico semanal de todos los repositorios activos de GitHub del usuario (`alvaroferrufino`).
* **2. ¿Qué input necesita el agente?:** 
  * **Datos de entrada:** Listado de repositorios públicos y privados mediante la GitHub CLI (`gh repo list`, `gh api` / `git log`).
  * **Contexto previo:** Utiliza la identidad de Chaski (`SOUL.md`) y el perfil técnico del usuario (`USER.md`) para enfocar el resumen en ingeniería de IA y desarrollo de software.
* **3. ¿Cómo es un buen output?:** 
  * **Formato y destino:** Un reporte ejecutivo formateado en viñetas enviado directamente por **Telegram** (y opcionalmente respaldado como borrador en Google Docs).
  * **Criterio de éxito:** El mensaje llega puntualmente los lunes a las 18:00 con la actividad de la semana agrupada por proyecto, sin requerir modificaciones manuales.

---

## 2. `daily-ops-briefing`

* **1. ¿Qué hace esta skill? (Una frase):** 
  Entrega una vista ejecutiva matutina combinando la agenda del día, las tareas pendientes y las comunicaciones prioritarias de la bandeja de entrada.
* **2. ¿Qué input necesita el agente?:** 
  * **Datos de entrada:** Eventos del calendario principal en Google Calendar (`Europe/Zurich`), tareas activas de Google Tasks y correos sin leer relevantes en Gmail.
  * **Contexto previo:** Se apoya en `TOOLS.md` para conocer los calendarios y canales por defecto, y en `AGENTS.md` para respetar los límites de lectura estricta sin enviar respuestas automáticas.
* **3. ¿Cómo es un buen output?:** 
  * **Formato y destino:** Un mensaje estructurado por bloques horarios y prioridades enviado por **Telegram**.
  * **Criterio de éxito:** Permite al usuario visualizar su jornada de un solo vistazo al iniciar el día.

---

## 3. `smart-doc-drafter`

* **1. ¿Qué hace esta skill? (Una frase):** 
  Estructura documentación técnica, planes o correos formales bajo estándares rigurosos de ingeniería y gestión de procesos.
* **2. ¿Qué input necesita el agente?:** 
  * **Datos de entrada:** Instrucciones en lenguaje natural del usuario indicando el tema y el formato deseado (documento técnico, correo o reporte).
  * **Contexto previo:** Toma el estilo de redacción, tono profesional y firma configurados en `USER.md` y `SOUL.md`.
* **3. ¿Cómo es un buen output?:** 
  * **Formato y destino:** Un documento redactado en Google Docs o un borrador en Gmail guardado bajo la ruta de trabajo especificada (`OpenClaw_Workspace/...`).
  * **Criterio de éxito:** El documento respeta la estructura formal (resumen ejecutivo al inicio, desarrollo accionable y tono adecuado) requiriendo mínimas correcciones antes de su uso final.
