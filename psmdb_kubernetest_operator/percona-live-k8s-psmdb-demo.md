# Status of pods, persistent volumes, pvcs

watch kubectl get pods
watch kubectl get pv
watch kubectl get pvc

# Check to see if the minikube VM is running
minikube status -p minikube-docker

# Start the minikube VM
minikube start -p minikube-docker

# Start the minikube dashboard
minikube dashboard -p minikube-docker

# Check to see if the PSMDB namespace is running
kubectl get namespace

# Delete the PSMDB namespace
kubectl delete namespace psmdb

# Install the operator
z operator-0.3.0
kubectl apply -f deploy/crd.yaml
kubectl create namespace psmdb
kubectl config set-context $(kubectl config current-context) --namespace=psmdb
kubectl apply -f deploy/rbac.yaml
kubectl apply -f deploy/operator.yaml
kubectl apply -f deploy/mongodb-users.yaml
kubectl apply -f deploy/cr.yaml

# Delete a pod
kubectl delete pods lab1-minikube-rs0-2

# Connect to a pod
kubectl exec -it lab1-minikube-rs0-0 mongo

# Check MongoDB replica set
use admin
db.auth("clusterAdmin", "clusterAdmin123456")
rs.status()

# Delete primary pod
kubectl delete pods lab1-minikube-rs0-0

# Watch the pods rebuild

# Reconnect to pod
kubectl exec -it lab1-minikube-rs0-0 mongo

# Show it's now secondary
use admin
db.auth("clusterAdmin", "clusterAdmin123456")
rs.status()

# Scale operator
kubectl get psmdb/lab1-minikube -o yaml | sed -e 's/size: 3/size: 5/' | kubectl apply -f -
kubectl get psmdb/lab1-minikube -o yaml | sed -e 's/size: 5/size: 3/' | kubectl apply -f -

# Show PVs stay even after scaling down

# Edit deploy/cr.yaml file to change name and start second replica set
vim deploy/cr.yaml
kubectl apply -f deploy/cr.yaml

# Delete newly created replica set
kubectl delete psmdb lab1-minikube2

# Show that that PV/PVC stay

# Delete the PVCs
kubectl delete pvc mongod-data-lab1-minikube2-rs0-2
kubectl delete pvc mongod-data-lab1-minikube2-rs0-1
kubectl delete pvc mongod-data-lab1-minikube2-rs0-0

# Show that the PVs delete as well

# Delete the namespace
kubectl delete namespace psmdb

# Show pods/PV/PVCs delete

