# client-fl

![Version: 1.0.8](https://img.shields.io/badge/Version-1.0.8-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

Client for the federated learning application.

**Homepage:** <https://docs.ai4os.eu/en/latest/howtos/train/federated-flower.html>

## Source Code

* <https://github.com/InseeFrLab/helm-charts-interactive-services>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://sftobias.github.io/helm-charts-interactive-services | library-chart | 1.7.9 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| certificates | object | `{}` |  |
| chromadb.secretName | string | `""` |  |
| clientConfig.dataPath | string | `""` |  |
| clientConfig.endpoint | string | `""` |  |
| clientConfig.modelFile | string | `""` |  |
| clientConfig.modelPath | string | `""` |  |
| configEnvVars[0].name | string | `"END_POINT"` |  |
| configEnvVars[0].value | string | `"{{ .clientConfig.endpoint }}"` |  |
| configEnvVars[1].name | string | `"DATA_PATH"` |  |
| configEnvVars[1].value | string | `"{{ printf \"/home/%s/work/s3/%s/%s\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) (trimAll \"/\" .clientConfig.dataPath) }}"` |  |
| configEnvVars[2].name | string | `"MODEL_PATH"` |  |
| configEnvVars[2].value | string | `"{{ printf \"/home/%s/work/s3/%s/%s\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) (trimAll \"/\" .clientConfig.modelPath) }}"` |  |
| configEnvVars[3].name | string | `"MODEL_FILE"` |  |
| configEnvVars[3].value | string | `"{{ .clientConfig.modelFile }}"` |  |
| coresite.secretName | string | `""` |  |
| discovery.chromadb | bool | `true` |  |
| discovery.hive | bool | `true` |  |
| discovery.metaflow | bool | `true` |  |
| discovery.milvus | bool | `true` |  |
| discovery.mlflow | bool | `true` |  |
| environment.group | string | `"users"` |  |
| environment.user | string | `"onyxia"` |  |
| extraEnvVars | list | `[]` |  |
| fullnameOverride | string | `""` |  |
| git.branch | string | `""` |  |
| git.cache | string | `""` |  |
| git.email | string | `""` |  |
| git.enabled | bool | `false` |  |
| git.name | string | `""` |  |
| git.repository | string | `""` |  |
| git.secretName | string | `""` |  |
| git.token | string | `""` |  |
| global.suspend | bool | `false` |  |
| hive.secretName | string | `""` |  |
| imagePullSecrets | list | `[]` |  |
| ingress.annotations | list | `[]` |  |
| ingress.certManagerClusterIssuer | string | `""` |  |
| ingress.enabled | bool | `false` |  |
| ingress.hostname | string | `"deployments.cloud.eosc-siesta.eu"` |  |
| ingress.hosts[0] | string | `"deployments.cloud.eosc-siesta.eu"` |  |
| ingress.ingressClassName | string | `"nginx"` |  |
| ingress.secretName | string | `"deployments.cloud.eosc-siesta.eu-tls"` |  |
| ingress.tls | bool | `true` |  |
| ingress.useCertManager | bool | `false` |  |
| ingress.useTlsSecret | bool | `true` |  |
| ingress.userHostname | string | `"chart-example-user.local"` |  |
| init.personalInit | string | `""` |  |
| init.personalInitArgs | string | `""` |  |
| init.regionInit | string | `""` |  |
| init.standardInitPath | string | `""` |  |
| kubernetes.enabled | bool | `false` |  |
| kubernetes.role | string | `"view"` |  |
| message.en | string | `""` |  |
| message.fr | string | `""` |  |
| metaflow.secretName | string | `""` |  |
| milvus.secretName | string | `""` |  |
| mlflow.secretName | string | `""` |  |
| nameOverride | string | `""` |  |
| networking.clusterIP | string | `"None"` |  |
| networking.service.port | int | `8888` |  |
| networking.sparkui.port | int | `4040` |  |
| networking.type | string | `"ClusterIP"` |  |
| networking.user.enabled | bool | `false` |  |
| networking.user.port | int | `5000` |  |
| networking.user.ports | list | `[]` |  |
| nodeSelector."node.kubernetes.io/floating-ip" | string | `""` |  |
| openshiftSCC.enabled | bool | `false` |  |
| openshiftSCC.scc | string | `""` |  |
| persistence.accessMode | string | `"ReadWriteOnce"` |  |
| persistence.enabled | bool | `false` |  |
| persistence.size | string | `"10Gi"` |  |
| podAnnotations | object | `{}` |  |
| podSecurityContext.fsGroup | int | `100` |  |
| proxy.enabled | bool | `false` |  |
| proxy.httpProxy | string | `""` |  |
| proxy.httpsProxy | string | `""` |  |
| proxy.noProxy | string | `""` |  |
| replicaCount | int | `1` |  |
| repository.condaRepository | string | `""` |  |
| repository.configMapName | string | `""` |  |
| repository.pipRepository | string | `""` |  |
| resources | object | `{}` |  |
| route.annotations | list | `[]` |  |
| route.enabled | bool | `false` |  |
| route.hostname | string | `"chart-example.local"` |  |
| route.tls.termination | string | `"edge"` |  |
| route.userHostname | string | `"chart-example-user.local"` |  |
| route.wildcardPolicy | string | `"None"` |  |
| s3.accessKeyId | string | `""` |  |
| s3.defaultRegion | string | `""` |  |
| s3.enabled | bool | `false` |  |
| s3.endpoint | string | `""` |  |
| s3.pathStyleAccess | bool | `false` |  |
| s3.secretAccessKey | string | `""` |  |
| s3.secretName | string | `""` |  |
| s3.sessionToken | string | `""` |  |
| s3.workingDirectoryPath | string | `""` |  |
| security.allowlist.enabled | bool | `false` |  |
| security.allowlist.ip | string | `"0.0.0.0/0"` |  |
| security.networkPolicy.enabled | bool | `false` |  |
| security.networkPolicy.from | list | `[]` |  |
| security.password | string | `"changeme"` |  |
| securityContext | object | `{}` |  |
| service.image.custom.enabled | bool | `false` |  |
| service.image.custom.version | string | `"harbor.cloud.eosc-siesta.eu/siesta/client-fl"` |  |
| service.image.pullPolicy | string | `"Always"` |  |
| service.image.version | string | `"harbor.cloud.eosc-siesta.eu/siesta/client-fl"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| startupProbe.failureThreshold | int | `60` |  |
| startupProbe.initialDelaySeconds | int | `10` |  |
| startupProbe.periodSeconds | int | `10` |  |
| startupProbe.successThreshold | int | `1` |  |
| startupProbe.timeoutSeconds | int | `2` |  |
| tolerations | list | `[]` |  |
| userPreferences.darkMode | bool | `false` |  |
| userPreferences.language | string | `"en"` |  |
| vault.directory | string | `""` |  |
| vault.enabled | bool | `false` |  |
| vault.mount | string | `""` |  |
| vault.secret | string | `""` |  |
| vault.secretName | string | `""` |  |
| vault.token | string | `""` |  |
| vault.url | string | `""` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
