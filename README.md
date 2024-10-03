# datacache


Setup a node pool for data cache

```sh
export CLUSTER_NAME="data-cache-test"
export ZONE="us-central1-c"
export PROJECT="anthos-multi-cloud-335819"


gcloud container node-pools create --cluster ${CLUSTER_NAME} datacache --num-nodes=1 --local-nvme-ssd-block count=2    --zone ${ZONE} --machine-type=n2-standard-2 --node-labels=datacache-storage-gke-io=enabled

```

Apply the storage class
```sh
kubectl apply -f data-cache-storageclass.yaml
```
