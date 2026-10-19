# OCS · Ambiente de prueba

Organizaciones Comunitarias y Subvenciones (PROEXSI). Versión de demostración con datos ficticios en memoria: organizaciones con su directiva y socios, proyectos, subvenciones con su paso por el Concejo, decretos, pagos, rendiciones y fiscalizaciones.

- Usuarios: `admin` y `rgutierrez` (administración), `mtorres` (organizaciones), `ncampos` (subvenciones), `gibarra` (Secretaría Municipal), `fvalenzuela` (finanzas), `cperez` y `vrivas` (Dirección de Control), `auditor` (consulta) · Clave: `CambiarEsta2026`
- Los datos se reinician cada vez que el servicio se reinicia.
- Se publica en Render como *Web Service* con Docker (plan gratuito).

## Publicar o actualizar en Render

1. Cree un repositorio `ocs-prueba` (GitHub o GitLab) con estos tres archivos: `Dockerfile`, `ocs-app.tar.gz` y este `README.md`.
2. En Render: **New › Web Service**, conecte el repositorio, *Runtime* **Docker**, plan **Free**. No necesita variables adicionales.
3. Para actualizar, reemplace `ocs-app.tar.gz` por el de la nueva entrega y haga *commit*: Render vuelve a desplegar solo.
4. El plan gratuito se suspende tras 15 minutos sin uso; el primer ingreso después tarda cerca de un minuto en despertar.

`ocs-app.tar.gz` es la publicación de `OCS.Web` compilada en modo demostración (`dotnet publish src/OCS.Web -c Release -p:Demo=true`).
