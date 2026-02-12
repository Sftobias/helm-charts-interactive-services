# uc1-agents-model

![Version: 1.0.8](https://img.shields.io/badge/Version-1.0.8-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

Agent-based epidemic simulation model designed to study the dynamics of vector-borne diseases in spatially explicit environments.

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://sftobias.github.io/helm-charts-interactive-services | library-chart | 1.7.4 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| affinity | object | `{}` |  |
| autoscaling.enabled | bool | `false` |  |
| autoscaling.maxReplicas | int | `100` |  |
| autoscaling.minReplicas | int | `1` |  |
| autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| certificates | object | `{}` |  |
| environment.group | string | `"users"` |  |
| environment.user | string | `"onyxia"` |  |
| extraEnvVars[0].name | string | `"FILE_MODEL"` |  |
| extraEnvVars[0].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/model_SIESTA_0_13012025.json"` |  |
| extraEnvVars[10].name | string | `"FILENAME_TT_UNI"` |  |
| extraEnvVars[10].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/tt_universidad.csv"` |  |
| extraEnvVars[11].name | string | `"PATH_POPULATION_INPUT"` |  |
| extraEnvVars[11].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/population/"` |  |
| extraEnvVars[12].name | string | `"OUT_PATH_PREPROCESSOR"` |  |
| extraEnvVars[12].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/outputs/out_data_preprocessor"` |  |
| extraEnvVars[13].name | string | `"OUT_PATH_PREVIOUS_PARAMETRIZATION"` |  |
| extraEnvVars[13].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/outputs/out_data_previous_parametrization"` |  |
| extraEnvVars[14].name | string | `"OUT_PATH_DAY_SIMULATOR"` |  |
| extraEnvVars[14].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/outputs/out_data_day_simulator"` |  |
| extraEnvVars[15].name | string | `"OUT_PATH_DATA_PREPARATION_STEP_SIMULATOR"` |  |
| extraEnvVars[15].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/outputs/out_data_preparation_step_simulator"` |  |
| extraEnvVars[16].name | string | `"OUT_PATH_STEP_SIMULATOR"` |  |
| extraEnvVars[16].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/outputs/out_data_step_simulator"` |  |
| extraEnvVars[1].name | string | `"FILE_DENSITIES_MOSQUITOS"` |  |
| extraEnvVars[1].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/df_mosquito_weekly_densities.csv"` |  |
| extraEnvVars[2].name | string | `"FILENAME_CELLS"` |  |
| extraEnvVars[2].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/ine_cells/celdas_marzo_2020.shp"` |  |
| extraEnvVars[3].name | string | `"FILENAME_MOB"` |  |
| extraEnvVars[3].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/ine_mobility/ine_data.csv"` |  |
| extraEnvVars[4].name | string | `"FILENAME_MEANS_TRANS"` |  |
| extraEnvVars[4].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/means_transport_per_mun_type_norm.csv"` |  |
| extraEnvVars[5].name | string | `"FILENAME_TRIPS_PER_HOUR_DES"` |  |
| extraEnvVars[5].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/n_trips_per_hour_des.csv"` |  |
| extraEnvVars[6].name | string | `"FILENAME_TRIPS"` |  |
| extraEnvVars[6].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/probs_by_age_ntrips.csv"` |  |
| extraEnvVars[7].name | string | `"FILENAME_TT_CONTINUA_COMPLETO"` |  |
| extraEnvVars[7].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/tt_continua_completo.csv"` |  |
| extraEnvVars[8].name | string | `"FILENAME_TT_CONTINUA_PARCIAL"` |  |
| extraEnvVars[8].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/tt_continua_parcial.csv"` |  |
| extraEnvVars[9].name | string | `"FILENAME_TT_PARTIDA_COMPLETO"` |  |
| extraEnvVars[9].value | string | `"{{ .s3.workingDirectoryPath }}/uc1_data/tt_partida_completo.csv"` |  |
| fullnameOverride | string | `""` |  |
| global.suspend | bool | `false` |  |
| imagePullSecrets[0].name | string | `"harbor-robot-secret"` |  |
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
| kubernetes.enabled | bool | `false` |  |
| kubernetes.role | string | `"view"` |  |
| message.en | string | `""` |  |
| message.fr | string | `""` |  |
| nameOverride | string | `""` |  |
| networking.clusterIP | string | `"None"` |  |
| networking.service.port | int | `3000` |  |
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
| repository.pipRepository | string | `""` |  |
| resources | object | `{}` |  |
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
| service.image.custom.version | string | `"harbor.cloud.eosc-siesta.eu/siesta/ubuntu22"` |  |
| service.image.pullPolicy | string | `"IfNotPresent"` |  |
| service.image.version | string | `"harbor.cloud.eosc-siesta.eu/siesta/uc1-mobagents:1.0.0"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |
| tolerations | list | `[]` |  |
| userPreferences.darkMode | bool | `false` |  |
| userPreferences.language | string | `"en"` |  |

----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
