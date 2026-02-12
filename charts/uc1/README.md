# uc1-agents-model

![Version: 1.0.19](https://img.shields.io/badge/Version-1.0.19-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square)

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
| configEnvVars[0].name | string | `"FILE_MODEL"` |  |
| configEnvVars[0].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/model_SIESTA_0_13012025.json\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[10].name | string | `"IN_DATA_TT_UNI"` |  |
| configEnvVars[10].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/tt_universidad.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[11].name | string | `"IN_DATA_POP"` |  |
| configEnvVars[11].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/population/\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[12].name | string | `"OUT_PREPROCESSOR"` |  |
| configEnvVars[12].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/outputs/out_data_preprocessor\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[13].name | string | `"OUT_PREVIOUS_PARAMETRIZATION"` |  |
| configEnvVars[13].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/outputs/out_data_previous_parametrization\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[14].name | string | `"OUT_DAY_SIMULATOR"` |  |
| configEnvVars[14].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/outputs/out_data_day_simulator\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[15].name | string | `"OUT_DATA_PREPARATION_STEP_SIMULATOR"` |  |
| configEnvVars[15].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/outputs/out_data_preparation_step_simulator\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[16].name | string | `"OUT_STEP_SIMULATOR"` |  |
| configEnvVars[16].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/outputs/out_data_step_simulator\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[1].name | string | `"FILE_DENSITIES"` |  |
| configEnvVars[1].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/df_mosquito_weekly_densities.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[2].name | string | `"IN_DATA_CELLS"` |  |
| configEnvVars[2].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/ine_cells/celdas_marzo_2020.shp\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[3].name | string | `"IN_DATA_MOB"` |  |
| configEnvVars[3].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/ine_mobility/ine_data.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[4].name | string | `"IN_DATA_TRANS"` |  |
| configEnvVars[4].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/means_transport_per_mun_type_norm.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[5].name | string | `"IN_DATA_TRIPS_HOURLY"` |  |
| configEnvVars[5].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/n_trips_per_hour_des.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[6].name | string | `"IN_DATA_TRIPS"` |  |
| configEnvVars[6].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/probs_by_age_ntrips.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[7].name | string | `"IN_DATA_CON_COMPLETO"` |  |
| configEnvVars[7].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/tt_continua_completo.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[8].name | string | `"IN_DATA_CON_PARCIAL"` |  |
| configEnvVars[8].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/tt_continua_parcial.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| configEnvVars[9].name | string | `"IN_DATA_PARTIDA_COMPLETO"` |  |
| configEnvVars[9].value | string | `"{{ printf \"/home/%s/work/s3/%s/uc1_data/tt_partida_completo.csv\" .environment.user (trimAll \"/\" .s3.workingDirectoryPath) }}"` |  |
| environment.group | string | `"users"` |  |
| environment.user | string | `"onyxia"` |  |
| extraEnvVars | list | `[]` |  |
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
