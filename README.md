# flux-playground
Play with weaveworks/flux

## Setup

```bash
$ kubectl create clusterrolebinding "cluster-admin-$(whoami)" --clusterrole=cluster-admin --user="$(gcloud config get-value core/account)"
$ kubectl apply -f weave
$ kubectl apply -f weave/flux
$ kubectl get po -n weave
NAME                                    READY     STATUS    RESTARTS   AGE
weave-flux-agent-6b4cd5c498-64fsn       1/1       Running   0          2s
weave-flux-memcached-754fb5f596-pwqqh   1/1       Running   0          29m

$ kubectl logs -n weave weave-flux-agent-6b4cd5c498-64fsn
## Copy the public key from the logs and set it up as a deploy key in GitHub.
```