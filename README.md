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


## kubectl commmand list
- `kubectl help | more`
- `kubectl cluster-info`
- `kubectl config current-context`
- `kubectl get pods --all-namespaces`
- `kubectl apply -f pod.yml` deploy a pod into a cluster
- `kubectl get pods --all-namespaces`
- `kubectl get pods --watch`
- `kubectl get pods -o wide` this command show in each nodes the pods are running on
- `kubectl get pods --show-labels`
- `kubectl describe pods hello-pod`
- `kubectl delete -f multi-pod.yml`
- `kubectl delete pod hello-pod`
- `kubectl apply -f svc-nodeport.yml`
- `kubectl expose pod hello-pod --name=hello-svc --target-port=8080 --type=NodePort` expose a service NodePort type
- `kubectl get services`
- `kubectl delete svc hello-svc` delete svc object
- `kubectl describe svc ps-nodeport`
- `kubectl get deploy` check it out deployment status
- `kubectl delete deploy web-deploy`
- `kubectl create deployment myapp --image manojnair/myapp:v1` creating deployment imperatively 
- `kubectl expose deployment myapp --type=LoadBalancer --port=80 --target-port=80` create / expose service type LB imperatively 
- `kubectl get deployments`
- `kubectl scale deployment myapp --replicas=3` scale up
- `kubectl get rs` check it out replica set status
- `kubectl get ep` list of endpoint
- `kubectl rollout status deploy web-deploy` check rollout/update status
- `kubectl rollout history deploy web-deploy` check rollout/update history 
- `kubectl rollout undo deploy web-deploy --to-revision=1` rollback to specific revision, higher the revision number new it is