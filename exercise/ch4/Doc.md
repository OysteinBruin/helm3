### Part 1: Install helm chart with none templating for a single application

1. Create a kubernetes cluster with [kind](https://kind.sigs.k8s.io/)  
- `kind create cluster --name helm helm3-course`

![Command line image](/_img/ch4/kind-create-cluster.png)

2. Install helm chart  
- `helm install demo-guestbook guestbook`

![Command line image](/_img/ch4/helm-install.png)

3. Ugrade helm chart after manually updating docker image and helm yml files  

Note the different paths where the commands are executed from.  
- `docker build -f Dockerfile -t phico/frontend:1.1 .`  
- `helm upgrade demo-guestbook guestbook`

![Command line image](/_img/ch4/helm-upgrade.png)

4. Uninstall helm chart 
 
- `helm uninstall demo-guestbook`

![Command line image](/_img/ch4/helm-uninstall.png)