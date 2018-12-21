#### How to Install the Helm Chart

This chart requires `githubkey` and `webhookSecret` to be defined. These values are sensitive and should not be stored in a public place. Create a values.yaml file or set the values for `githubkey` and `webhookSecret` using `--set`

1. Create the namespace in which this app will be deployed; namespace.yaml creates *bulldozer* namespace. 
   * `kubectl apply -f namespace.yaml`
2. Install the helm chart to the *bulldozer* namespace created.
   * `helm install --name bulldozer ./bulldozer -f <values/file/path> --namespace=bulldozer`

   This install the bot in the *bulldozer* namespace with *bulldozer* as the helm release name.
   
3. To delete the helm release do following-
   * `helm del --purge bulldozer`
