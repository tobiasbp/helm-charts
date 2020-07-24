# helm-charts
A repository for Helm charts. The dir `charts` contains the chart source files, and the dir `repo`
contains the packages to be shared at _https://charts.balle-petersen.org_.

# How to add a package

* Add new chart in `charts/your-chart`
* Go to dir `repo`
* Build package: `helm package ../charts/your-chart`
* Update index: `helm repo index . --url https://charts.balle-petersen.org`
* Update master branch
