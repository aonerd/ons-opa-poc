# ons-opa-poc


Create NameSpace and deploy service

```
❯ k create ns opal-ns
namespace/opal-ns created

❯ ./build-local.sh
```


On this repo:
```

cd ons-opa-poc/helm

helm install -f values.yaml -n opal-ns opal .


❯ helm install -f values.yaml -n opal-ns opal .
W0219 22:08:13.329608   41276 warnings.go:70] spec.template.spec.containers[0].env[2]: hides previous definition of "OPAL_SERVER_URL", which may be dropped when using apply
NAME: opal
LAST DEPLOYED: Wed Feb 19 22:08:13 2025
NAMESPACE: opal-ns
STATUS: deployed
REVISION: 1


```



Useful commands

```
# ❯ helm install -f values.yaml -n opal-ns opal .

# ❯ helm upgrade -f values.yaml -n opal-ns opal .

# ❯ kubectl run -i --tty --rm debug --image=curlimages/curl:8.12.1 --restart=Never -- sh

```