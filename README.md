# JENKINS ON KUBERNETES
![469-jenkins@4x](https://github.com/ArgoFox1/JenkinsOnKubernetes/assets/105239243/a476427c-0978-4f50-9d50-fd5cf2fe352d)
![kubectl-logo-medium](https://github.com/ArgoFox1/JenkinsOnKubernetes/assets/105239243/d9c775e7-df19-4856-8d26-4c47fb4bf7b1)

# GUIDE 

1-**Pull project with github**
>git clone https://github.com/ArgoFox1/JenkinsOnKubernetes

2-**Go to the project folder**
>cd/path/to/your/folder

3-**Start the kubernetes**
>minikube start

4-**If you can't find a namespace named jenkins, create one**
>kubectl create namespace jenkins

5-**Create deployment object**
>kubectl apply -f jenkins-deployment.yaml -n jenkins

6-**Check deployment object**
>kubectl get deployment -n jenkins

7-**Get the password in the logs of the deployment object's pod**
>**Get pod name**
>>kubectl get pod -n jenkins

>>**Get password**
>>>kubectl logs podname -n jenkins

**Its gives you log like this Jenkins initial setup is required. An admin user has been created and a password generated.
      Please use the following password to proceed to installation:
      this is your password :bexcadxxdx0149exacafe9e215e0107x**

8-**Then create service object**
>kubectl apply -f jenkins-service.yaml -n jenkins

9-**Get you minikube ip and your kubernetes port**
>minikube ip
>>kubectl get service -n jenkins

10-**Combine IP and Port**
>ip:port

11-**Put your ip and port like this**
![Screenshot from 2024-07-01 12-29-55](https://github.com/ArgoFox1/JenkinsOnKubernetes/assets/105239243/0f1b11a5-43f9-4ab7-9f53-cff38902ded0)

12-**and it will ask you for your admin password.**
![Ekran görüntüsü 2024-07-01 213200](https://github.com/ArgoFox1/JenkinsOnKubernetes/assets/105239243/8eba2877-74f9-44c5-bc98-732fce74b846)

13-**When installation and signing up completes This page will welcomes you**
![Screenshot from 2024-07-01 11-40-59](https://github.com/ArgoFox1/JenkinsOnKubernetes/assets/105239243/55dac019-b02c-4d3c-ba6d-2d758e1d8e5e)

