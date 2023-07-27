# kubernetes-pluralsights

- getting kubernetes
    - kubectl used to manage clusters
    - cloud providers
        - linode 
        - google cloud `gcloud auth login`

## commmand list - docker
- `docker login`
- `docker image build -t juniorhc/getting-started-k8s:1.0 .`
- `docker image push juniorhc/getting-started-k8s:1.0 `


## commmand list - k8s
- `kubectl cluster-info`
- `kubectl apply -f pod.yml` deploy a pod into a cluster
- `kubectl get pods --watch`
- `kubectl get pods -o wide`
- `kubectl describe pods hello-pod`
- `kubectl delete -f multi-pod.yml`
- `kubectl expose pod hello-pod --name=hello-svc --target-port=8080 --type=NodePort` expose a service NodePort type
- `kubectl get services`
- `kubectl delete svc hello-svc` delete svc object