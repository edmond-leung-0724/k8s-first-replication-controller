1) Create pod

kubectl create -f nginx-rc.yaml

kubectl get pods

kubectl get po -l app=nginx-app

kubectl describe rc nginx-rc

2) Shutdown Node (Node Fail)

kubectl get po -o wide

Shutdown 1 node

kubectl get nodes

Auto create new pod in another node

kubectl get po -o wide

3) Scaling up

kubectl scale rc nginx-rc --replicas=5

kubectl get rc nginx-rc

kubectl get po -o wide

4) Scaling down

kubectl scale rc nginx-rc --replicas=3

kubectl get rc nginx-rc

kubectl get po -o wide

5) Delete

kubectl delete -f nginx-rc.yaml

kubectl get rc

kubectl get po -l app=nginx-app
