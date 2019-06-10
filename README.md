## Deploy with `kubectl`

```
kubectl kustomize overlays | kubectl apply -f -
```

## Deploy with `kapp`

```
wget https://github.com/k14s/kapp/releases/download/v0.7.0/kapp-darwin-amd64
install kapp-darwin-amd64 /usr/local/bin/kapp
rm -f kapp-darwin-amd64
```

```
kubectl kustomize overlays | kapp -y deploy -a scdf -f -

or

kapp deploy -a scdf -f <(kubectl kustomize overlays)
```

<p align="center">
    <img src="https://raw.githubusercontent.com/making/spring-cloud-dataflow-kustomize/master/docs/termtosvg_fzcvycgo.svg">
</p>

```
kapp inspect -a scdf -t
kapp logs -f -a scdf
```