# Demo for Deploying LKE Cluster from Jenkins

## Create Kubenetes Cluster on Linode and Connect to it

![image](https://user-images.githubusercontent.com/18715119/235320145-1406a9a4-773d-4a29-8dc9-670ea8299dc4.png)
![image](https://user-images.githubusercontent.com/18715119/235320192-a88edbcc-6d8f-4b9d-a934-d84577193138.png)
![image](https://user-images.githubusercontent.com/18715119/235320270-4f8339dd-c813-487a-ade6-65fe8bda6354.png)
![image](https://user-images.githubusercontent.com/18715119/235320329-d634e868-5f93-4643-9cf7-380e16ed9a99.png)

The kubeconfig file which is generated can be downloaded.

    # If we want to point kubectl to another location, we can set the 
    # KUBECONFI env variable to the address of another config file.
    export KUBECONFIG=~/test-kubeconfig.yaml
    
    # We can cconfirm that we are connected to Linode.
    kubectl get node
     # NAME                            STATUS   ROLES    AGE     VERSION
     # lke105686-157961-644d6b99af77   Ready    <none>   5m10s   v1.26.3
     
    
## Add LKE Credentials to Jenkins
![image](https://user-images.githubusercontent.com/18715119/235320561-133fd0fa-b955-48d0-8c5b-30ec98229fdc.png)
![image](https://user-images.githubusercontent.com/18715119/235320580-b129a561-b74e-4b5b-af6b-713fc1727f84.png)

Subsequently, we install the plugin to help us to use the kubeconfig file to execute kubectl commands.
