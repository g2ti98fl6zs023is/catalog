# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env | object | See below | environment variables. See [image docs](https://docs.linuxserver.io/images/docker-wikijs#environment-variables-e) for more details. |
| env.DB_TYPE | string | `"postgres"` | Set the container timezone |
| envValueFrom.DB_HOST.secretKeyRef.key | string | `"plainhost"` |  |
| envValueFrom.DB_HOST.secretKeyRef.name | string | `"dbcreds"` |  |
| envValueFrom.DB_PASS.secretKeyRef.key | string | `"postgresql-password"` |  |
| envValueFrom.DB_PASS.secretKeyRef.name | string | `"dbcreds"` |  |
| image.pullPolicy | string | `"IfNotPresent"` | image pull policy |
| image.repository | string | `"tccr.io/truecharts/wikijs"` | image repository |
| image.tag | string | `"v2.5.274@sha256:0e7dbe27ba2cebe9c193f172c642fc84af0cad79b5901eaccf2c19d217c3d3f7"` | image tag |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| postgresql.enabled | bool | `true` |  |
| postgresql.existingSecret | string | `"dbcreds"` |  |
| postgresql.postgresqlDatabase | string | `"wikijs"` |  |
| postgresql.postgresqlUsername | string | `"wikijs"` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service | object | See values.yaml | Configures service settings for the chart. |

All Rights Reserved - The TrueCharts Project
