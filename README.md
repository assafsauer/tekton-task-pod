** quick guide **

```
kubectl create secret docker-registry dockercred -n default \
    --docker-server=https://index.docker.io/v1/ \
    --docker-username=asauer \
    --docker-password=xxxx \
    --docker-email=email
