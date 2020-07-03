# This shows the steps to do Jenkins configuration on a kubernetes cluster
## Pre-requisites are
[Single-node-cluster-creation](https://kubernetes.io/docs/setup/production-environment/tools/kubeadm/create-cluster-kubeadm/)
[Single-node-cluster-in-VM](https://blog.e-zest.com/installing-kubernetes-cluster-on-ubuntu)

## Steps to set-up Jenkins
- Clone kubernetes-deployment project from github
- Create Jenkins namespace using "kubectl create ns jenkins"
- Execute kubectl apply -n jenkins -f jenkins/
- Watch the jenkins pod using "kubectl get pods -n jenkins -w"
- Once pods are up and running access jenkins using "<node-ip>:30003"
- Get the password using "kubectl logs <pod-jenkins-xxxx -n jenkins" copy the password
- paste the password in Jenkins UI and install required Jenkins plugins
- Restart Jenkins
