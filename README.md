# k8s
Creating Kubernetes Cluster in Cloud 

 

1. Create Personal Account in Azure or GCP 

 

1.1 Configure DNS for later usage 

 

- Zone Name: `{{ StudentShortName }}.playpit.net` (example: `sbeliakou.playpit.net`) 

- Send NS details to Siarhei Beliakou for sub-domain delegation 

 

2. Create Kubernetes Cluster using any solution in Cloud Account 

 

2.1 Clusters: 

- Production (1 master, 3 workers) 

- Staging (1 master, 1 worker) 

 

2.2 Configure kubectl Client Access to clusters 

 

3. Make Sure Cluster has Necessary Components Installed: 

 

3.1 Ingress Controller 

 

3.1.1 Nginx Ingress Controller:  

- https://github.com/kubernetes/ingress-nginx/blob/master/docs/deploy/index.md 

- Traefik? 

- Certmanager (LetsEncrypt)? 

 

3.1.2 Create wildcard A record for Nginx Ingress Controller SVC (LoadBalancer IP) 

 

- Prod Cluster: `*.{{ StudentShortName }}.playpit.net` 

- Staging Cluster: `*.np.{{ StudentShortName }}.playpit.net` 

 

3.2 Cloud Autoscaler 

3.3 Metrics Server 

3.4 Kubernetes Dashboard 

Simple/aka default kuberentes dashboard 

Weave Dashboard 

 

3. Deploy Application Stack into your Kubernetes Clusters 

 

3.1 Microservice Application 

- https://microservices-demo.github.io/ 

- Configure Pod AntiAffinity? 

 

3.2 Configure public access to this application with Ingress rule(s) 

 

- Prod Environment: `socks-shop.{{ StudentShortName }}.playpit.net` 

- Staging Environment: `socks-shop.np.{{ StudentShortName }}.playpit.net` 

 

3.3 Disable all backdoors to your application (NodePorts and so on) 

===============================================================================

Examples: 

PHP Guest Book 

Application:  https://kubernetes.io/docs/tutorials/stateless-application/guestbook/ 

Logging:  https://kubernetes.io/docs/tutorials/stateless-application/guestbook-logs-metrics-with-elk/ 

Configuration: 

Network Policies 

https://kubernetes.io/docs/concepts/services-networking/network-policies/ 

Pod Security: 

https://kubernetes.io/docs/concepts/policy/pod-security-policy/  

https://kubernetes.io/docs/tasks/configure-pod-container/security-context/ 

Pod Priority & Disruption: 

https://kubernetes.io/docs/concepts/configuration/pod-priority-preemption/ 

https://kubernetes.io/docs/concepts/workloads/pods/disruptions/ 

Resource Quotas & QoS: 

https://kubernetes.io/docs/concepts/policy/resource-quotas/ 

https://kubernetes.io/docs/concepts/configuration/manage-resources-containers/ 

https://kubernetes.io/docs/tasks/configure-pod-container/quality-service-pod/ 

HPA: 

https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale/ 

https://kubernetes.io/docs/tasks/run-application/horizontal-pod-autoscale-walkthrough/ 

Liveness, Readiness and Startup Probes: 

https://kubernetes.io/docs/tasks/configure-pod-container/configure-liveness-readiness-startup-probes/ 

Deployment Strategies: 

https://blog.container-solutions.com/kubernetes-deployment-strategies 

https://www.bluematador.com/blog/kubernetes-deployments-rolling-update-configuration 

https://blog.container-solutions.com/deployment-strategies 

 

Useful Addons: 

KubeDB: 

https://kubedb.com/ 

KubeCost: 

https://kubecost.com/ 

Kube2IAM (AWS): 

https://github.com/jtblin/kube2iam  

https://www.bluematador.com/blog/iam-access-in-kubernetes-installing-kube2iam-in-production 

External DNS: 

https://github.com/kubernetes-sigs/external-dns  

https://www.digitalocean.com/community/tutorials/how-to-automatically-manage-dns-records-from-digitalocean-kubernetes-using-externaldns 

EventRouter: 

https://docs.openshift.com/container-platform/4.5/logging/cluster-logging-eventrouter.html 

Kube-Monkey 

https://www.padok.fr/en/blog/kube-monkey-kubernetes 

https://github.com/asobti/kube-monkey 

 


