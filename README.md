**Deploying a Sample Nginx Application on Kubernetes**

* A running Kubernetes cluster.
* kubectl command-line tool configured to access your cluster.

**Steps**

1. Create deployment.yml for a nginx application.
2. Create service.yml to expose the nginx application.
3. Apply the deployment and service configurations
    kubectl apply -f deployment.yaml
    kubectl apply -f service.yaml
4. check the pod status.
     kubectl get pod
5.  check the service status.
    kubectl get svc
6. kubectl port-forward pod/my-nginx-576c6b7b6-vqxnx 18000:80
7. Verify that the application is running and accessible.
![image](https://github.com/user-attachments/assets/61b0f859-f467-4dcb-bcc3-806cb5292a31)
8.  Scale the deployment to run multiple replicas of the application 
     kubectl scale deployment my-nginx --replicas=3
9. Application is running with the specified number of replicas.
     kubectl get pods
10. Check the logs of the application:
   kubectl logs my-nginx-576c6b7b6-cdh8p
![image](https://github.com/user-attachments/assets/041c38b9-a646-4276-bde3-5bc0ba5cf316)


