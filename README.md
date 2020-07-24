# helm-charts
A repository for Helm charts. The dir `charts` contains the chart source files, and the dir `repo`
contains the packages to be shared at _https://charts.balle-petersen.org_.

# How to use the repository with Helm

* Add the repository: `helm repo add charts.balle-petersen.org https://charts.balle-petersen.org`
* Confirm repository is in list of repositories: `helm repo list`


# How to add a package to the repository

* Add new chart in `charts/your-chart`
* Go to dir `repo`
* Build package: `helm package ../charts/your-chart`
* Update index: `helm repo index . --url https://charts.balle-petersen.org`
* Update master branch

