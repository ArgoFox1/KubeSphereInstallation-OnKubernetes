# KubeSphereOnKubernetes
![37326490](https://github.com/ArgoFox1/KubeSphereOnKubernetes/assets/105239243/ccb16be8-c56a-4998-9a5b-440e3a2f6497)

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
![Screenshot from 2024-07-02 03-08-46](https://github.com/ArgoFox1/KubeSphereOnKubernetes/assets/105239243/1eb6f5a6-8334-453a-b40e-60ccfceba8c4)

5-**After that, this page will welcome you**
![Screenshot from 2024-07-02 02-57-54](https://github.com/ArgoFox1/KubeSphereOnKubernetes/assets/105239243/a8df37ba-8586-49fd-99be-0f99d9a36945)
