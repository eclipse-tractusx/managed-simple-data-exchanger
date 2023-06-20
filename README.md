## Helm chart for Simple-Data-Exchanger

This helm chart installs the SDE application which consists of
     
   * [Frontend](https://github.com/catenax-ng/tx-managed-simple-data-exchanger-frontend)
   * [Backend](https://github.com/catenax-ng/tx-managed-simple-data-exchanger-backend) 
    

## Installation

To install the chart with the release name portal:

``` $ helm repo add tractusx-dev https://eclipse-tractusx.github.io/charts/dev ```

```$ helm install sde tractusx-dev/sde```

## Requirements

| Repository                                         | Name       | Version  |
|--------------------------------------------------- |------------|--------- |
| `https://charts.bitnami.com/bitnami`               | postgresql | 11.9.13  |                     
	
