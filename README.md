# datacache


Setup a node pool for data cache

```sh
export CLUSTER_NAME=""
export ZONE=""
export PROJECT=""


gcloud container node-pools create --cluster ${CLUSTER_NAME} datacache-node-pool4 --num-nodes=1 --local-nvme-ssd-block count=2    --zone ${ZONE} --machine-type=n2-standard-8 --node-labels=datacache-storage-gke-io-ramdsk=enabled

```

Apply the storage class
```sh
kubectl apply -f data-cache-storageclass.yaml
```
