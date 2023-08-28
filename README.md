** quick guide **

```diff
1) creat docker secret for the kaniko 
kubectl create secret docker-registry dockercred -n default \
    --docker-server=https://index.docker.io/v1/ \
    --docker-username=asauer \
    --docker-password=xxxx \
    --docker-email=email

2) update Configmap with the vars in the configmap.yaml

3) execute script from a POD steps.sh
https://github.com/apigee/devrel/tree/main/tools/hybrid-quickstart
```

<img width="714" alt="image" src="https://github.com/assafsauer/tekton-task-pod/assets/22165556/798b3682-b879-4fa2-a5ca-a9c8c344cbc5">


