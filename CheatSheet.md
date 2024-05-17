
### Commands

#### Create a Resource from a Manifest

```shell
kubectl create -f manifest.yaml
```

#### Delete a Resource from a Manifest

```shell
kubectl delete -f manifest.yaml
```

#### Create or Update a Resource from a Manifest

```shell
kubectl apply -f manifest.yaml
```

#### Delete a Resource

```shell
kubectl delete resource_type resource_name
```

#### Exporting a Resource as Manifest

```shell
kubectl get resource_type resource_name -o format --export
```

#### Port Forward `localhost` to a Pod

```shell
kubectl port-forward pod_name local_port:container_port
```

#### Describing a Resource

```shell
kubectl describe resource_type resource_name
```


#### Creating a Namespace with `kubectl`

```shell
kubectl create namespace namespace_name
```

#### Listing Resources within a Namespace

```shell
kubectl -n namespace_name get pods
```

#### Setting Explicit Namespace for Context

```shell
kubectl config set-context context_name --namespace namespace_name
```

#### Create, or Update, Helm Release

```shell
helm upgrade --install -f values.yaml release_name chart_repository/chart_name
```

#### Deleting a Helm Release

```shell
helm delete release_name
```

#### Purging a Helm Release

```shell
helm delete --purge release_name
```

#### Add New Repository

```shell
helm repo add repository_name repository_uri
```

#### Creating a New Chart

```shell
helm create
```

#### Generate the underlying YAML files using Template

```shell
helm template --help
helm template -f telegraf.values.yaml influxdata/telegraf --output-dir abc123
```

#### Generate Manifests with Kustomize

```shell
kustomize build ./directory
```

#### Apply Manifests with Kustomize

```shell
kustomize build ./directory | kubectl -f -
```




### Links

- [Kubernetes Documentation](https://kubernetes.io/docs/)

- [Influx Helm Charts](https://github.com/influxdata/helm-charts)

- [Artefact Helm packages](https://artifacthub.io/packages/search?ts_query_web=influx&sort=relevance&page=1)

- [TOML to YAML](https://transform.tools/toml-to-yaml)