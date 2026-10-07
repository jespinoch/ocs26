# Prospección OCS 26

Aplicación móvil para preparar cotizaciones de máquinas de café e insumos. La pestaña **Datos** incorpora una consola SQLite local: permite ejecutar SQL, ver resultados como tabla y gráfico, y exportarlos a CSV.

## Datos en el dispositivo

La base `prospectos` se guarda en IndexedDB del navegador. Incluye registros de demostración y las cotizaciones que guardes desde la pantalla de cotización. La información no se envía a un servidor. Puedes consultar, por ejemplo:

```sql
SELECT empresa, ciudad, tazas_mes, total
FROM prospectos
ORDER BY total DESC;
```

Abre la aplicación desde un sitio HTTPS o un servidor local para que el navegador permita almacenamiento persistente. El motor SQLite se incluye en `vendor/` para que la consola no dependa de una CDN. Su licencia está en `vendor/sql.js.LICENSE`.
