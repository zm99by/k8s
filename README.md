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
