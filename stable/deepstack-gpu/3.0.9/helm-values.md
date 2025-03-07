# Default Helm-Values

TrueCharts is primarily build to supply TrueNAS SCALE Apps.
However, we also supply all Apps as standard Helm-Charts. In this document we aim to document the default values in our values.yaml file.

Most of our Apps also consume our "common" Helm Chart.
If this is the case, this means that all values.yaml values are set to the common chart values.yaml by default. This values.yaml file will only contain values that deviate from the common chart.
You will, however, be able to use all values referenced in the common chart here, besides the values listed in this document.

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| env.MODE | string | `"High"` |  |
| env.MODELSTORE-DETECTION | string | `"{{ .Values.persistence.modelstore.mountPath }}"` |  |
| env.PUID | int | `568` |  |
| env.USER_ID | string | `"{{ .Values.env.PUID }}"` |  |
| env.VISION-DETECTION | string | `"True"` |  |
| env.VISION-FACE | string | `"True"` |  |
| env.VISION-SCENE | string | `"True"` |  |
| image.pullPolicy | string | `"IfNotPresent"` |  |
| image.repository | string | `"tccr.io/truecharts/deepstack-gpu"` |  |
| image.tag | string | `"v2021.09.1@sha256:f924cebf518a54bca2ca2ac33911cf3af4dd7403cad371781422436ce4254a28"` |  |
| persistence.data.enabled | bool | `true` |  |
| persistence.data.mountPath | string | `"/datastore"` |  |
| persistence.modelstore.enabled | bool | `true` |  |
| persistence.modelstore.mountPath | string | `"/modelstore/detection"` |  |
| podSecurityContext.runAsGroup | int | `0` |  |
| podSecurityContext.runAsUser | int | `0` |  |
| securityContext.readOnlyRootFilesystem | bool | `false` |  |
| securityContext.runAsNonRoot | bool | `false` |  |
| service.main.ports.main.port | int | `10050` |  |
| service.main.ports.main.targetPort | int | `5000` |  |

All Rights Reserved - The TrueCharts Project
