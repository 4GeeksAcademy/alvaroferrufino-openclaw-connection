* **Objetivo:** Consolidar el progreso técnico de todos los repositorios del usuario (`alvaroferrufino`) sin limitarse a un único proyecto.
* **Disparadores:**
  * **Manual:** *"Resume mi avance en GitHub"*, *"¿Cómo van mis repos?"*
  * **Programado:** Todos los lunes a las 18:00 (`Europe/Zurich`).
* **Herramientas utilizadas:**
  * GitHub CLI (`gh repo list`, `gh api` / `git log`) en modo solo lectura.
  * **Telegram** (entrega de resumen ejecutivo) y/o **Google Docs** vía Zapier.
* **Flujo de ejecución:**
  1. Listar todos los repositorios activos de `alvaroferrufino` con actividad reciente.
  2. Extraer commits y cambios de los últimos 7 días agrupados por repositorio.
  3. Sintetizar cada proyecto con fecha del último cambio, hitos y estado actual.
  4. Enviar reporte por **Telegram**.
