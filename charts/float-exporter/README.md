# float-exporter
An exporter of metrics from the [API at float.com](https://dev.float.com/) to be consumed by Prometheus. Read about the configuration
and metrics at the exporter's Git repository: https://github.com/tobiasbp/float_exporter

# How to install the Chart
How to install the chart from the _balle-petersen_ repository. For adding the repository, read instructions [here](https://github.com/tobiasbp/helm-charts).

1. Create API token in Float
2. Install the package: `helm install my-float-exporter balle-petersen/float-exporter --set accessToken="MY_TOKEN" --set email="me@example.com" `
3. Add the exporter to you Prometheus configuration as described when the chart has been installed

