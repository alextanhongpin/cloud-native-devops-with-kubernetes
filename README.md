## Deploying the service

```bash
# Build the docker image.
$ docker build -t go-demo

# Deploy the service.
$ k apply -f .

# Get the service nodePort to call.
$ k get svc
```

Output:

```bash
NAME         TYPE        CLUSTER-IP     EXTERNAL-IP   PORT(S)          AGE
demo         NodePort    10.108.51.16   <none>        9999:31378/TCP   37s
kubernetes   ClusterIP   10.96.0.1      <none>        443/TCP          48d
```

## Call the service
```bash
$ curl localhost:31378
```

Output:
```bash
Hello world
```
