# Latidos

Latido de las colas de trabajo de Yard (yard.heavylisting.com), Live (live.heavylisting.com), el CRM
(crm.pruebalucuma.site) y Publisher (publisher.pruebalucuma.site, programador de publicaciones). Reemplaza a cron-job.org, que no llega a esos sitios.

- Programación: cada 5 minutos, 4 latidos por pasada (≈1 por minuto).
- Secrets del repo: `YARD_CRON_TOKEN` (= `CRON_TOKEN` de Yard en Plesk) `CRM_CRON_TOKEN` (= `CRON_TOKEN` del CRM) y
  `PUBLISHER_CRON_TOKEN` (= `CRON_TOKEN` de Publisher).
  Si falta uno, ese sitio se salta. Live no lleva token.
- Probar a mano: Actions → Latidos → Run workflow.
- Una vez al día se vuelve a habilitar el workflow para que GitHub no lo apague por inactividad (60 días).
