## Deploy with `kubectl`

```
kubectl kustomize overlays | kubectl apply -f -
```

## Deploy with `kapp`

[Install kapp](https://k14s.io/#install)

```
brew tap k14s/tap
brew install kapp
```

```
kubectl kustomize overlays | kapp -y deploy -a scdf -f -

or

kapp deploy -a scdf -f <(kubectl kustomize overlays)
```

[![asciicast](https://asciinema.org/a/zKf5e6VTFkvPrTnBLhkY7uijc.svg)](https://asciinema.org/a/zKf5e6VTFkvPrTnBLhkY7uijc)

```
kapp inspect -a scdf -t
kapp logs -f -a scdf
```
