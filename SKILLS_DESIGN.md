# SKILLS_DESIGN.md - Arquitectura de Skills Operativas de Chaski

Este documento define las habilidades reutilizables (skills) diseñadas para **Chaski**, alineadas con la configuración de `~/.openclaw/workspace` (`AGENTS.md`, `USER.md` y `TOOLS.md`).

---

## 1. `github-weekly-digest` (Resumen Multi-Repositorio de GitHub)

* **Objetivo:** Consolidar el progreso técnico de todos los repositorios del usuario (`alvaroferrufino`) sin limitarse a un único proyecto.
* **Disparadores:**
  * **Manual:** *"Resume mi avance en GitHub"*, *"¿Cómo van mis repos?"*
  * **Programado:** Todos los lunes a las 18:00 (`Europe/Zurich`).
* **Herramientas utilizadas:**
  * GitHub CLI (`gh repo list`, `gh api` / `git log`) en modo solo lectura.
  * **Telegram** (entrega de resumen ejecutivo) y/o **Google Docs** vía Zapier (archivado semanal).
* **Flujo de ejecución:**
  1. Listar todos los repositorios activos de `alvaroferrufino` con actividad reciente.
  2. Extraer los commits y cambios de los últimos 7 días agrupados por repositorio.
  3. Sintetizar cada proyecto con: fecha del último cambio, resumen de hitos clave y estado actual.
  4. Enviar el reporte formateado en viñetas por **Telegram** (o generar borrador en **Google Docs** bajo `OpenClaw_Workspace/YYYY-MM-DD_GitHub_Digest`).
* **Límites de seguridad (`AGENTS.md`):** Ejecución autónoma (solo lectura y reporte interno al propio usuario). No realiza commits ni modificaciones remotas.

---

## 2. `daily-ops-briefing` (Briefing Diario de Operaciones y Agenda)

* **Objetivo:** Entregar una vista ejecutiva accionable al inicio de la jornada combinando agenda, tareas pendientes y comunicaciones prioritarias.
* **Disparadores:**
  * **Manual:** *"Dame mi briefing de hoy"*, *"¿Qué tengo pendiente hoy?"*
  * **Programado (opcional):** Lunes a viernes a las 08:00 (`Europe/Zurich`).
* **Herramientas utilizadas:**
  * **Google Calendar**, **Google Tasks** y **Gmail** (vía Zapier).
  * **Telegram** (canal de entrega).
* **Flujo de ejecución:**
  1. Consultar eventos del día en el calendario `primary` (`Europe/Zurich`).
  2. Listar tareas activas o con vencimiento próximo en **Google Tasks** (`Mis tareas`).
  3. Revisar correos sin leer relevantes en **Gmail** (académicos, operativos o urgentes) sin modificar su estado.
  4. Consolidar en un mensaje breve con bloques horarios, top 3 prioridades y alertas, enviándolo por **Telegram**.
* **Límites de seguridad (`AGENTS.md`):** Lectura autónoma. Nunca responde ni envía correos sin confirmación explícita.

---

## 3. `smart-doc-drafter` (Generador de Entregables y Borradores Profesionales)

* **Objetivo:** Estructurar documentación técnica, planes de estudio o comunicaciones formales siguiendo estándares de ingeniería y gestión de procesos.
* **Disparadores:**
  * **Manual:** *"Prepara un documento sobre..."*, *"Redacta un correo para..."*
* **Herramientas utilizadas:**
  * **Google Docs**, **Google Drive** y **Gmail** (vía Zapier).
* **Flujo de ejecución:**
  1. Identificar el formato requerido (documento técnico en Google Docs o correo en Gmail) y el idioma (español por defecto o inglés según contexto).
  2. Estructurar el contenido con resumen ejecutivo al inicio, desarrollo accionable y firma estándar si es correo (`Alvaro Ferrufino`).
  3. Guardar como borrador en **Google Drive** (`OpenClaw_Workspace/YYYY-MM-DD_Nombre_Descriptivo`) o como borrador en **Gmail**.
  4. **Detenerse y solicitar confirmación explícita** antes de enviar correos o compartir archivos con terceros.
* **Límites de seguridad (`AGENTS.md`):** Prohibido el envío externo o compartición pública sin aprobación previa del usuario.
