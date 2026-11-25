# Latidos

Latido de las colas de trabajo de Yard (yard.heavylisting.com), Live (live.heavylisting.com), el CRM
(crm.pruebalucuma.site) y Publisher (publisher.pruebalucuma.site, programador de publicaciones). Reemplaza a cron-job.org, que no llega a esos sitios.

- **Continuo** (desde 2026-11-24): cada ejecución late cada 60 s durante ~5 h 45 min y se relanza sola.
  El `schedule` de GitHub (cada 5 min en teoría) corría en la práctica cada 4-12 h: queda solo de respaldo
  para rearrancar la cadena si se corta. Es normal ver ejecuciones largas y algunas "cancelled".
- Secrets del repo: `YARD_CRON_TOKEN` (= `CRON_TOKEN` de Yard en Plesk) `CRM_CRON_TOKEN` (= `CRON_TOKEN` del CRM) y
  `PUBLISHER_CRON_TOKEN` (= `CRON_TOKEN` de Publisher).
  Si falta uno, ese sitio se salta. Live no lleva token.
- Probar a mano: Actions → Latidos → Run workflow.
- Una vez al día se vuelve a habilitar el workflow para que GitHub no lo apague por inactividad (60 días).
