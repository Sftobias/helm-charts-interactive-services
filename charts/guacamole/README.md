# guacamole

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 1.6.0](https://img.shields.io/badge/AppVersion-1.6.0-informational?style=flat-square)

Apache Guacamole remote desktop gateway (guacamole + guacd + postgres)

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://sftobias.github.io/helm-charts-interactive-services | library-chart | 1.7.9 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| environment.group | string | `"users"` |  |
| environment.user | string | `"onyxia"` |  |
| extraEnvVars | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| global.suspend | bool | `false` |  |
| guacamole.extensions | string | `""` |  |
| guacd.image | string | `"linuxserver/guacd:latest"` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | list | `[]` |  |
| ingress.certManagerClusterIssuer | string | `""` |  |
| ingress.enabled | bool | `true` |  |
| ingress.hostname | string | `"deployments.cloud.eosc-siesta.eu"` |  |
| ingress.hosts[0] | string | `"deployments.cloud.eosc-siesta.eu"` |  |
| ingress.ingressClassName | string | `"nginx"` |  |
| ingress.secretName | string | `"deployments.cloud.eosc-siesta.eu-tls"` |  |
| ingress.tls | bool | `true` |  |
| ingress.useCertManager | bool | `false` |  |
| ingress.useTlsSecret | bool | `true` |  |
| ingress.userHostname | string | `"chart-example-user.local"` |  |
| initdb.backoffLimit | int | `6` |  |
| initdb.enabled | bool | `true` |  |
| kubernetes.enabled | bool | `false` |  |
| kubernetes.role | string | `"view"` |  |
| message.en | string | `""` |  |
| message.fr | string | `""` |  |
| nameOverride | string | `""` |  |
| networking.clusterIP | string | `""` |  |
| networking.service.port | int | `80` |  |
| networking.service.targetPort | int | `8080` |  |
| networking.type | string | `"ClusterIP"` |  |
| networking.user.enabled | bool | `false` |  |
| networking.user.port | int | `5000` |  |
| networking.user.ports | list | `[]` |  |
| nodeSelector | object | `{}` |  |
| openshiftSCC.enabled | bool | `false` |  |
| openshiftSCC.scc | string | `""` |  |
| persistence.drive.accessMode | string | `"ReadWriteMany"` |  |
| persistence.drive.enabled | bool | `true` |  |
| persistence.drive.size | string | `"2Gi"` |  |
| persistence.drive.storageClassName | string | `""` |  |
| persistence.postgres.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.postgres.enabled | bool | `true` |  |
| persistence.postgres.size | string | `"10Gi"` |  |
| persistence.postgres.storageClassName | string | `""` |  |
| persistence.record.accessMode | string | `"ReadWriteMany"` |  |
| persistence.record.enabled | bool | `true` |  |
| persistence.record.size | string | `"5Gi"` |  |
| persistence.record.storageClassName | string | `""` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext.fsGroup | int | `100` |  |
| postgres.database | string | `"guacamole_db"` |  |
| postgres.image | string | `"postgres:13.4"` |  |
| postgres.password | string | `"guacamole"` |  |
| postgres.pgdata | string | `"/var/lib/postgresql/data/guacamole"` |  |
| postgres.username | string | `"guacamole"` |  |
| replicaCount | int | `1` |  |
| repository.condaRepository | string | `""` |  |
| repository.configMapName | string | `""` |  |
| repository.packageManagerUrl | string | `""` |  |
| repository.pipRepository | string | `""` |  |
| repository.rRepository | string | `""` |  |
| resources.guacamole | object | `{}` |  |
| resources.guacd | object | `{}` |  |
| resources.initdb | object | `{}` |  |
| resources.postgres | object | `{}` |  |
| route.annotations | list | `[]` |  |
| route.enabled | bool | `false` |  |
| route.hostname | string | `"chart-example.local"` |  |
| route.tls.termination | string | `"edge"` |  |
| route.userHostname | string | `"chart-example-user.local"` |  |
| route.wildcardPolicy | string | `"None"` |  |
| security.allowlist.enabled | bool | `false` |  |
| security.allowlist.ip | string | `"0.0.0.0/0"` |  |
| security.networkPolicy.enabled | bool | `false` |  |
| security.networkPolicy.from | list | `[]` |  |
| security.password | string | `"changeme"` |  |
| securityContext | object | `{}` |  |
| service.image.custom.enabled | bool | `false` |  |
| service.image.custom.version | string | `"guacamole/guacamole:latest"` |  |
| service.image.pullPolicy | string | `"Always"` |  |
| service.image.version | string | `"guacamole/guacamole:latest"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| userPreferences.darkMode | bool | `false` |  |
| userPreferences.language | string | `"en"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
