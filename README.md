** quick guide **

```
1) creat docker secret for the kaniko 
kubectl create secret docker-registry dockercred -n default \
    --docker-server=https://index.docker.io/v1/ \
    --docker-username=asauer \
    --docker-password=xxxx \
    --docker-email=email

2) update Configmap with the vars in the configmap.yaml

3) execute script from a POD steps.sh
https://github.com/apigee/devrel/tree/main/tools/hybrid-quickstart


<img width="695" alt="image" src="https://github.com/assafsauer/tekton-task-pod/assets/22165556/2264b222-5018-4eae-a7aa-8322be85def7">
