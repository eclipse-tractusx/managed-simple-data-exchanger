# sde

![Version: 0.1.1](https://img.shields.io/badge/Version-0.1.1-informational?style=flat-square) ![Type: application](https://img.shields.io/badge/Type-application-informational?style=flat-square) ![AppVersion: 2.3.1](https://img.shields.io/badge/AppVersion-2.3.1-informational?style=flat-square)

A Helm chart for Kubernetes

## Source Code

* <https://github.com/eclipse-tractusx/managed-simple-data-exchanger>

## Requirements

| Repository | Name | Version |
|------------|------|---------|
| https://charts.bitnami.com/bitnami | sdepostgresql(postgresql) | 12.12.10 |

## Values

| Key | Type | Default | Description |
|-----|------|---------|-------------|
| backend.affinity | object | `{}` |  |
| backend.autoscaling.enabled | bool | `false` |  |
| backend.autoscaling.maxReplicas | int | `100` |  |
| backend.autoscaling.minReplicas | int | `1` |  |
| backend.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| backend.backend.endpoints.default.path | string | `"/backend"` | The path mapping the "default" api is going to be exposed at |
| backend.backend.endpoints.default.port | string | `"7070"` | The network port, which the "default" api is going to be exposed by the container, pod and service |
| backend.configuration.properties | string | `"keycloak.clientid=default\nspring.security.oauth2.resourceserver.jwt.issuer-uri=default\nmanagement.endpoint.health.probes.enabled=true\nmanagement.health.readinessstate.enabled=true\nmanagement.health.livenessstate.enabled=true\nmanagement.endpoints.web.exposure.include=*\nspring.lifecycle.timeout-per-shutdown-phase=30s\nlogging.level.org.springframework.security.web.csrf=INFO\nspring.servlet.multipart.enabled=true\nspring.main.allow-bean-definition-overriding=true\nspring.servlet.multipart.file-size-threshold=2KB\nspring.servlet.multipart.max-file-size=200MB\nspring.servlet.multipart.max-request-size=215MB\nserver.servlet.context-path=/api\nspring.flyway.baseline-on-migrate=true\nspring.flyway.locations=classpath:/flyway\nspring.datasource.driver-class-name=org.postgresql.Driver\nspring.jpa.hibernate.ddl-auto=update\nspring.jpa.open-in-view=false\nfile.upload-dir=./temp/\nlogging.level.org.apache.http=info\nlogging.level.root=info\ndigital-twins.hostname=default\ndigital-twins.authentication.url=default\ndigital-twins.authentication.clientId=default\ndigital-twins.authentication.clientSecret=default\ndigital-twins.authentication.grantType=client_credentials\nedc.hostname=default\nedc.apiKeyHeader=default\nedc.apiKey=default\nedc.consumer.hostname=default\nedc.consumer.apikeyheader=default\nedc.consumer.apikey=default\nedc.consumer.datauri=/api/v1/ids/data\ndft.hostname=default\ndft.apiKeyHeader=default\ndft.apiKey=default\nmanufacturerId=default\npartner.pool.hostname=default\nconnector.discovery.token-url=default\nconnector.discovery.clientId=default\nconnector.discovery.clientSecret=default\nportal.backend.hostname=default\nspringdoc.api-docs.path=/api-docs"` |  |
| backend.fullnameOverride | string | `""` |  |
| backend.image.pullPolicy | string | `"Always"` |  |
| backend.image.repository | string | `"tractusx/managed-simple-data-exchanger-backend"` |  |
| backend.image.tag | string | `""` |  |
| backend.imagePullSecrets | list | `[]` |  |
| backend.ingresses[0].annotations | object | `{}` |  |
| backend.ingresses[0].certManager | object | `{"clusterIssuer":"letsencrypt-prod"}` | If present overwrites the default secret name |
| backend.ingresses[0].certManager.clusterIssuer | string | `"letsencrypt-prod"` | If preset enables certificate generation via cert-manager cluster-wide issuer |
| backend.ingresses[0].className | string | `"nginx"` |  |
| backend.ingresses[0].enabled | bool | `false` |  |
| backend.ingresses[0].endpoints[0] | string | `"default"` |  |
| backend.ingresses[0].hostname | string | `""` |  |
| backend.ingresses[0].tls.enabled | bool | `true` |  |
| backend.ingresses[0].tls.secretName | string | `""` |  |
| backend.nameOverride | string | `""` |  |
| backend.nodeSelector | object | `{}` |  |
| backend.podAnnotations | object | `{}` |  |
| backend.podSecurityContext.fsGroup | int | `2000` |  |
| backend.portContainer | int | `8080` |  |
| backend.resources.limits.cpu | string | `"600m"` |  |
| backend.resources.limits.memory | string | `"2Gi"` |  |
| backend.resources.requests.cpu | string | `"600m"` |  |
| backend.resources.requests.memory | string | `"2Gi"` |  |
| backend.securityContext.allowPrivilegeEscalation | bool | `false` |  |
| backend.securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| backend.securityContext.readOnlyRootFilesystem | bool | `true` |  |
| backend.securityContext.runAsNonRoot | bool | `true` |  |
| backend.securityContext.runAsUser | int | `1001` |  |
| backend.service.port | int | `7070` |  |
| backend.service.targetPort | int | `8080` |  |
| backend.service.type | string | `"ClusterIP"` |  |
| backend.tolerations | list | `[]` |  |
| frontend.affinity | object | `{}` |  |
| frontend.autoscaling.enabled | bool | `false` |  |
| frontend.autoscaling.maxReplicas | int | `100` |  |
| frontend.autoscaling.minReplicas | int | `1` |  |
| frontend.autoscaling.targetCPUUtilizationPercentage | int | `80` |  |
| frontend.configuration.properties | string | `"REACT_APP_API_URL=\nREACT_APP_KEYCLOAK_URL=\nREACT_APP_KEYCLOAK_REALM=\nREACT_APP_CLIENT_ID=\nREACT_APP_FILESIZE=\nREACT_APP_DEFAULT_COMPANY_BPN="` |  |
| frontend.fullnameOverride | string | `""` |  |
| frontend.image.pullPolicy | string | `"Always"` |  |
| frontend.image.repository | string | `"tractusx/managed-simple-data-exchanger-frontend"` |  |
| frontend.image.tag | string | `""` |  |
| frontend.imagePullSecrets | list | `[]` |  |
| frontend.ingresses[0].annotations."kubernetes.io/tls-acme" | string | `"true"` |  |
| frontend.ingresses[0].certManager.clusterIssuer | string | `"letsencrypt-prod"` | If preset enables certificate generation via cert-manager cluster-wide issuer |
| frontend.ingresses[0].className | string | `"nginx"` |  |
| frontend.ingresses[0].enabled | bool | `false` |  |
| frontend.ingresses[0].endpoints[0] | string | `"default"` |  |
| frontend.ingresses[0].hostname | string | `""` |  |
| frontend.ingresses[0].tls.enabled | bool | `true` |  |
| frontend.ingresses[0].tls.secretName | string | `""` |  |
| frontend.nameOverride | string | `""` |  |
| frontend.nodeSelector | object | `{}` |  |
| frontend.podAnnotations | object | `{}` |  |
| frontend.podSecurityContext.fsGroup | int | `2000` |  |
| frontend.portContainer | int | `8080` |  |
| frontend.resources.limits.cpu | string | `"600m"` |  |
| frontend.resources.limits.memory | string | `"2Gi"` |  |
| frontend.resources.requests.cpu | string | `"600m"` |  |
| frontend.resources.requests.memory | string | `"2Gi"` |  |
| frontend.sde.endpoints.default.path | string | `"/"` | The path mapping the "default" api is going to be exposed at |
| frontend.sde.endpoints.default.port | string | `"80"` | The network port, which the "default" api is going to be exposed by the container, pod and service |
| frontend.securityContext.allowPrivilegeEscalation | bool | `false` |  |
| frontend.securityContext.capabilities.drop[0] | string | `"ALL"` |  |
| frontend.securityContext.readOnlyRootFilesystem | bool | `true` |  |
| frontend.securityContext.runAsNonRoot | bool | `true` |  |
| frontend.securityContext.runAsUser | int | `1000` |  |
| frontend.service.port | int | `80` |  |
| frontend.service.targetPort | int | `8080` |  |
| frontend.service.type | string | `"ClusterIP"` |  |
| frontend.tolerations | list | `[]` |  |
| replicaCount | int | `1` |  |
| sdepostgresql.auth.database | string | `"sdedb"` |  |
| sdepostgresql.auth.existingSecret | string | `"sde-postgresql-secrets"` |  |
| sdepostgresql.auth.port | int | `5432` |  |
| sdepostgresql.auth.secretKeys.adminPasswordKey | string | `"postgres-password"` |  |
| sdepostgresql.auth.secretKeys.userPasswordKey | string | `"password"` |  |
| sdepostgresql.auth.username | string | `"sdeuser"` |  |
| sdepostgresql.enabled | bool | `true` | PostgreSQL chart configuration Switch to enable or disable the PostgreSQL helm chart |
| sdepostgresql.fullnameOverride | string | `"product-sde-postgres"` |  |
| serviceAccount.annotations | object | `{}` |  |
| serviceAccount.create | bool | `true` |  |
| serviceAccount.name | string | `""` |  |


## Notice for Docker image

This application provides container images for demonstration purposes.

DockerHub: https://hub.docker.com/r/tractusx/managed-simple-data-exchanger-backend

DockerHub: https://hub.docker.com/r/tractusx/managed-simple-data-exchanger-frontend 

Eclipse Tractus-X product(s) installed within the image:

- GitHub: https://github.com/eclipse-tractusx/managed-simple-data-exchanger
- Project home: https://projects.eclipse.org/projects/automotive.tractusx
- Project license: [Apache License, Version 2.0] https://github.com/eclipse-tractusx/managed-simple-data-exchanger/blob/main/LICENSE

As with all Docker images, these likely also contain other software which may be under other licenses (such as Bash, etc from the base distribution, along with any direct or indirect dependencies of the primary software being contained).

As for any pre-built image usage, it is the image user's responsibility to ensure that any use of this image complies with any relevant licenses for all software contained within.
----------------------------------------------
Autogenerated from chart metadata using [helm-docs v1.11.0](https://github.com/norwoodj/helm-docs/releases/v1.11.0)
