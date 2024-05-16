## SDE Simple-Data-Exchanger

What is SDE?
In order to allow Data Providers and Data Consumers to easily participate in relevant Use Cases, a service for low-effort data sharing was needed. The service would add a convenience layer around already established CX components, such as EDC and Digital Twin Registry, simplifying their use.

It consists of two repositories Backend and Frontend.
   * [managed-simple-data-exchanger-frontend](https://github.com/eclipse-tractusx/managed-simple-data-exchanger-frontend) 
   * [managed-simple-data-exchanger-backend](https://github.com/eclipse-tractusx/managed-simple-data-exchanger-backend) 

for more information [DOCS](https://github.com/eclipse-tractusx/managed-simple-data-exchanger-frontend/blob/main/docs/Arc42.md)


## Helm chart for Simple-Data-Exchanger

This helm chart installs the SDE application which consists of backend and frontend configuration.
   * [charts](https://github.com/eclipse-tractusx/managed-simple-data-exchanger/tree/main/charts/simpledataexchanger)
     
## Installation

To install the chart with the release name portal:

 ```shell
  helm repo add sde-repo https://eclipse-tractusx.github.io/charts/dev 
  helm search repo sde-repo/sde
  helm install -f your-values.yaml release-name sde/sde-app 
 ``` 
## Requirements

| Repository                                         | Name       | Version  |
|--------------------------------------------------- |------------|--------- |
| `https://charts.bitnami.com/bitnami`               | postgresql | 12.12.10 |                     
	
### Licenses
For used licenses, please see the [NOTICE](https://github.com/eclipse-tractusx/managed-simple-data-exchanger/blob/main/NOTICE.md).

### Documentation
 Docs reference link can be found here [docs](https://github.com/eclipse-tractusx/managed-simple-data-exchanger/blob/main/docs/Install.md).

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
