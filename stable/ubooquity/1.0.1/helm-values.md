# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.MAXMEM | int | `512` |  |
| env.PUID | int | `568` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/ubooquity"` |  |
| image.tag | string | `"v2.1.2"` |  |
| persistence.books.enabled | bool | `true` |  |
| persistence.books.mountPath | string | `"/books"` |  |
| persistence.comics.enabled | bool | `true` |  |
| persistence.comics.mountPath | string | `"/comics"` |  |
| persistence.config.enabled | bool | `true` |  |
| persistence.config.mountPath | string | `"/config"` |  |
| persistence.files.enabled | bool | `true` |  |
| persistence.files.mountPath | string | `"/files"` |  |
| persistence.varrun.enabled | bool | `true` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.admin.ports.admin.enabled | bool | `true` |  |
| service.admin.ports.admin.port | int | `2203` |  |
| service.admin.ports.admin.targetPort | int | `2203` |  |
| service.admin.ports.enabled | bool | `true` |  |
| service.main.ports.main.port | int | `2202` |  |
| service.main.ports.main.targetPort | int | `2202` |  |

All Rights Reserved - The TrueCharts Project
