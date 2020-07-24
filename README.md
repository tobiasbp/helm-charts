# helm-charts
A repository for Helm charts. The dir `charts` contains the chart source files, and the dir `repo`
contains the packages to be shared at _https://charts.balle-petersen.org_.

# How to use the repository with Helm

* Add the repository: `helm repo add balle-petersen https://charts.balle-petersen.org`
* Confirm repository is in list of repositories: `helm repo list`

# Packages
In the following, it is assumed you have added the Helm repository as described above.

## db-backup

## digitalocean-exporter
An exporter of metrics from DigitalOcean to be consumed by Prometheus. Read about the configuration
and metrics at the exporter's Git repository: https://github.com/metalmatze/digitalocean_exporter

1. Create read only token in DigitalOcean
2. Install the package: `helm install my-doe balle-petersen/digitalocean-exporter --set exporter.DIGITALOCEAN_TOKEN="MY_TOKEN"`
3. Add the exporter to you Prometheus configuration

## float-exporter
An exporter of metrics from the [API at float.com](https://dev.float.com/) to be consumed by Prometheus. Read about the configuration
and metrics at the exporter's Git repository: https://github.com/tobiasbp/float_exporter

1. Create API token in Float
2. Install the package: `helm install my-fe balle-petersen/float-exporter --set accessToken="MY_TOKEN" --set email="me@example.com" `
3. Add the exporter to you Prometheus configuration as described when the chart has been installed

# How to add a package to this repository

* Add new chart in `charts/your-chart`
* Go to dir `repo`
* Build package: `helm package ../charts/your-chart`
* Update index: `helm repo index . --url https://charts.balle-petersen.org`
* Update master branch

