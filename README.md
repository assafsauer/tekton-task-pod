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
