# KubeSphereOnKubernetes

># GUIDE FOR INSTALLATION

1-**Make sure you have kubectl and sufficient free disk space** 
>kubectl --version
>> free -g

1-**Start minikube**
> minikube start

2-**Pull the project from GitHub**
>kubectl apply -f https://github.com/kubesphere/ks-installer/releases/download/v3.4.1/kubesphere-installer.yaml
>>kubectl apply -f https://github.com/kubesphere/ks-installer/releases/download/v3.4.1/cluster-configuration.yaml

3-**Verify the installation (this takes a couple of minutes)**
>kubectl logs -n kubesphere-system $(kubectl get pod -n kubesphere-system -l 'app in (ks-install, ks-installer)' -o jsonpath='{.items[0].metadata.name}') -f

4-**Then it will give you a link, username (admin), and password (P@ssw0rd). Click the link and log in with the given username and password.**

5-**After that, this page will welcome you**
