# guacamole

Helm chart for Apache Guacamole on Onyxia.

## Components

- `guacamole` (web UI)
- `guacd` (proxy daemon)
- `postgres` (database)
- `initdb` job to initialize the Guacamole schema

## Main values

- `service.image.version`: Guacamole web image
- `guacd.image`: guacd image
- `postgres.*`: DB image and credentials
- `persistence.drive`, `persistence.record`, `persistence.postgres`: storage settings
- `extraEnvVars`: extra env vars injected into Guacamole container
