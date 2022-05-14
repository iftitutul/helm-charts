http-echo-chart
---------------

This Kubernetes helm chart deploys the Hashicorp `http-echo` docker image in kubernetes

### Helm Charts

- Create the namespace `http-echo-ns`
  
  `kubectl create namespace http-echo-ns`

  
- To install the chart with the release name `http-echo-app` in namespace `http-echo-ns`:

  ```
  git clone https://github.com/iftitutul/http-echo.git 
  helm install http-echo . --namespace=http-echo-ns --values helm-charts/values.yaml
  ```

- Check the template
  
  `helm template http-echo --dry-run --debug`

- Upgrade the Chart 

  `helm upgrade http-echo http-echo/ --namespace=http-echo-ns --values http-echo/values.yaml`

- Uninstall the Chart

  `helm delete http-echo`
  

