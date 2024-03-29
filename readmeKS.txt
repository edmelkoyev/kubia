$ kubectl cluster-info

  Kubernetes master is running at https://kubernetes.docker.internal:6443
  KubeDNS is running at https://kubernetes.docker.internal:6443/api/v1/namespaces/kube-system/services/kube-dns:dns/proxy

$ kubectl get nodes
  NAME             STATUS   ROLES    AGE   VERSION
  docker-desktop   Ready    master   42h   v1.14.8

$ kubectl describe node docker-desktop
  Long list of details for given node ...

$ kubectl describe node
  Long list of details ...

$ kubectl run kubia --image=edmelkoyev/kubia --port=8080 --generator=run-pod/v1

  replicationcontroller/kubia created

$ kubectl get pods
  NAME          READY   STATUS    RESTARTS   AGE
  kubia-lvh7j   1/1     Running   0          2m27s

$ kubectl describe pod
  Long list of details ...

$ kubectl expose rc kubia --type=LoadBalancer --name kubia-http
  service/kubia-http exposed

$ kubectl get services
  NAME         TYPE           CLUSTER-IP      EXTERNAL-IP   PORT(S)          AGE
  kubernetes   ClusterIP      10.96.0.1       <none>        443/TCP          43h
  kubia-http   LoadBalancer   10.101.209.26   localhost     8080:30254/TCP   2m17s


$ kubectl describe service kubia-http


$ kubectl get

$ kubectl api-resources

$ kubectl get replicationcontrollers
$ kubectl get rc
  NAME    DESIRED   CURRENT   READY   AGE
  kubia   1         1         1       85m

$ kubectl scale rc kubia --replicas=2



