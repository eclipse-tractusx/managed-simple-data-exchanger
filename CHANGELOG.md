# Changelog

New features, fixed bugs, known defects and other noteworthy changes to each release of the Simple-Data-Exchanger helm chart.

## 0.1.2
### Change
* changed to v2.3.2 docker image version.
* veracode vulnerability fix in AppV- 2.3.2.
* updated backend-deployment.yaml for condition check.
* helm lint workflow fix for dependency. 

## 0.1.1
### Change
* helm-lint workflow corrected.
* helm-chart bumped version to 0.1.1 

## 0.1.0 
### Added 
* PostgreSQL random password generation.
### Change
* changed to v2.3.1 docker image version.
* fixed custom user permission issue in docker image.
* Veracode vulnerability fix in AppV- 2.3.1

## 0.0.10 [non-release]
### Added 
* PostgreSQL random password generation.
### Change
* changed to v2.3.0 docker image version.

## 0.0.9
### Change
* changed to v2.1.1 docker image version.

## 0.0.8
### Change
* changed to v2.1.0 docker image version.
* docs folder added and read me updated.

### Technical Support
* added meta file of tractusx.

## 0.0.7
### Change
* changed to v2.0.11 docker image version.
* added license header.

## 0.0.6
### Change
* changed to v2.0.8 docker image version.
* configuration properties added for sdebackend.

## 0.0.5
### Change
* changed to v2.0.2 docker image version.
* configuration properties added for sdebackend.


## 0.0.4
### Change
* changed to v2.0.1 docker image version.
* enabled usage of existing secret values if secret exists: stops regeneration of random secret values.

### Technical Support
* added chart test workflow for lint and install.

## 0.0.2
### Change
* added product helm chart for SDE, combining frontend and backend chart.
* moved repository to eclipse-tractusx.
