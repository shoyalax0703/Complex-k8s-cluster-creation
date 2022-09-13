# Complex Kubernetes Cluster Creation with Vagrant

Step 1:- Clone the git repo using command
```
git clone https://github.com/kmitsolution/k8s.git
```
Step 2:- Open Git Repo and Go to k8s/K8s-Vagrant/ on command terminal

Step 3:- Install some vagrant plugins by running below command
```
vagrant plugin install vagrant-vbguest
```
Step 4:- Run below command to create Kubernetes Cluster (It will take around 10-15 mins)
```
vagrant up
```
Step 5:- Connect to Master server
```
vagrant ssh kmaster
```
Step 6:- Verify the cluster is in ready State
```
kubectl get nodes
```
Error cases
The connection to the server localhost:8080 was refused - did you specify the right host or port?
```
mkdir -p $HOME/.kube
```
```
cp /etc/kubernetes/admin.conf $HOME/.kube/config
```
```
sudo chown $(id -u):$(id -g) $HOME/.kube/config
```
export KUBECONFIG=$HOME/.kube/config
```
kubectl get nodes
```
Example output: 
<img width="1344" alt="Screen Shot 2022-09-13 at 12 32 35" src="https://user-images.githubusercontent.com/66551005/189801583-7ab83eb5-4ff6-46b2-9654-50c978d36adc.png">

Completed now you have one master node and 2 worker nodes !!!
