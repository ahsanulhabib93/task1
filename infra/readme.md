Installing light weight kubernetes distribution (Kind):
download the binaries from official kind page curl -Lo ./kind https://kind.sigs.k8s.io/dl/v0.14.0/kind-linux-amd64
Change the file permission to execute chmod +x kind
move the file to /usr/local/bin mv kind /usr/local/bin
Create one yaml file for one master and two worker node vi cluster-config.yaml
# three node (two workers) cluster config
kind: Cluster
apiVersion: kind.x-k8s.io/v1alpha4
nodes:
- role: control-plane
- role: worker
- role: worker
Create the kubernetes cluster kind create cluster --config=cluster-config.yaml
