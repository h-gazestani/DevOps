# Pod 

```diff
! this is test
+ this is second test
-       other tesst
* another one
```


# Pods command

+ To list the running containers within a pod,
```bash
kubectl get pods my-pod -o jsonpath='{range .status.containerStatuses[*]}{.name}{"\t"}{.state.running.startedAt}{"\n"}{end}'
my-centos	2023-06-12T05:15:40Z
my-nginx	2023-06-12T05:14:57Z
```