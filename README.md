# helm-charts
A repository for Helm charts. The dir `charts` contains the chart source files, and the dir `repo`
contains the packages to be shared at _https://charts.balle-petersen.org_.

# How to use the repository with Helm

* Add the repository: `helm repo add charts.balle-petersen.org https://charts.balle-petersen.org`
* Confirm repository is in list of repositories: `helm repo list`

# Packages

## db-backup

## digitalocean-exporter
An exporter of metrics from DigitalOcean to be consumed by Prometheus. Read about the configuration
and metrics at the exporter's Git repository: https://github.com/metalmatze/digitalocean_exporter

* Create read only token in Digital ocean web interface
* Install the package: `helm install my-doe charts.balle-petersen.org/digitalocean-exporter --set exporter.DIGITALOCEAN_TOKEN="MY_TOKEN"`
* Add the exporter to you Prometheus configuration

# How to add a package to the repository

* Add new chart in `charts/your-chart`
* Go to dir `repo`
* Build package: `helm package ../charts/your-chart`
* Update index: `helm repo index . --url https://charts.balle-petersen.org`
* Update master branch

