# flux-playground
Play with weaveworks/flux

## Setup

```bash
$ kubectl create clusterrolebinding "cluster-admin-$(whoami)" --clusterrole=cluster-admin --user="$(gcloud config get-value core/account)"
$ kubectl apply -f weave
$ kubectl apply -f weave/flux
```
