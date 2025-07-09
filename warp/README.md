1. Update `replicaCount` in `setup.yaml`.

```shell
kubectl apply -f setup.yaml
```

2. Edit the access key and secret in `secrets.yaml`.

```shell
kubectl apply -f secrets.yaml
```


3. Review `job.yaml`.
  - If you updated `replicaCount` in the first step, don't forget to update the value of `--warp-client`.

```shell
kubectl create -n warp -f job.yaml
kubectl logs -f -n warp -l app=warp-job
```
