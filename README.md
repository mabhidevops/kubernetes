This repository helps you to install kubernetes and create the pods,deployment, services, scaling containerization. 

Before you learn kubernetes please get knowledge on docker. 
Prerequities for playing with kubernetes.

1. Install docker based on your laptop requirement. https://docs.docker.com/engine/install/
2. Install kubernetes and kubectl. go through this link - https://kubernetes.io/docs/tasks/tools/install-kubectl-macos/

I have attached kubernetes architecture in repo. Please go through it once. And it divided into **control plane** and **data plane**.

**Control Plane:**

1.Kubernetes API Server
2.Scheduler
3.etcd
4.controller
5.cloud control manager

**data plane**.
1.kube-proxy
2.kubelet
3.container runtime

The above two plance components will play the kubernetes services. Please go through it each and one i will also explain here.

Example 1: Check if it is installed propely docker and kubernetes. Then create file name pod.yml in any directory. And copy code or clone and save it.

1. create pod with this command - kubectl apply -f pod.yml
2. check if it is created or not - kubectl get pods
   NAME                                READY   STATUS                  RESTARTS        AGE
nginx                               1/1     Running                 0               27m
nginx                               1/1     Running                 0               30m     10.244.0.49    minikube   <none>           <none>

4. Output should be same then pod is created and app is running. Now login to minikube and check app is up and running.
5. minikube ssh
6. curl -l 10.244.0.49
7. Output should be below

<!DOCTYPE html>
<html>
<head>
<title>Welcome to nginx!</title>
<style>
    body {
        width: 35em;
        margin: 0 auto;
        font-family: Tahoma, Verdana, Arial, sans-serif;
    }
</style>
</head>
<body>
<h1>Welcome to nginx!</h1>
<p>If you see this page, the nginx web server is successfully installed and
working. Further configuration is required.</p>

<p>For online documentation and support please refer to
<a href="http://nginx.org/">nginx.org</a>.<br/>
Commercial support is available at
<a href="http://nginx.com/">nginx.com</a>.</p>

<p><em>Thank you for using nginx.</em></p>
</body>
</html>

Note: This pod is created in cluster without any service so if you want to connect, you should login to minikube and use ip address to check the application.

   
