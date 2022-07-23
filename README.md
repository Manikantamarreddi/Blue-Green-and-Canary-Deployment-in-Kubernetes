# Blue-Green-and-Canary-Deployment-in-Kubernetes

Step1: Setup a Kubernetes Cluster. I have setup with one master node and two worker nodes.

Step2: Install Kubectl and configure kube/config file to communicate with your cluster api server. For now I have installed kubectl in my master machine only(This is not recommended)

step3: Make sure all the nodes are in ready state. You can verify this using kubectl get nodes command and all the nodes status should be ready.

step4: Create a manifest file mavenwebappdeployment.yml to deploy your application as pods(containers) managed by Deployment Controller. 

Step5: Create a NodePort service to access your application from outside or within the Cluster. I have created the Service in same manifest file.

Step6: Apply the manifest file to create Deployment and Services using the command 
       kubectl apply -f mavenwebappdeployment.yml

Step7: You can access your application via ELB that you need to configure with end points as the cluster nodes and NodePort.


