# EKS-Terraform-Jenkins


                    

1. Install Java for Jenkins.

2.  Install Jenkins.

3. Install Terraform.

4.  Install Kubernetes (K8s).

5.  Install AWS CLI.

Install the required plugins in Jenkins (Kubernetes, Terraform).

Configure the AWS access key and secret key in manage credentials.

 ![image](https://github.com/user-attachments/assets/a6c4f820-aabc-4019-a481-3a250369cbf7)



**Provide.tf**: Contains all required details for AWS cloud configuration.

![image](https://github.com/user-attachments/assets/6d9e0ddb-c3e5-437e-bdab-83aedefb8357)

 
**Vpc.tf**: Creates the VPC using the credentials specified in provide.tf
 
![image](https://github.com/user-attachments/assets/b7151a6f-b56b-498e-bffd-1bb504dd4f33)


**eks.tf**: Creates the EKS cluster using the VPC created above and the credentials from provide.tf.
 
![image](https://github.com/user-attachments/assets/ce082a03-c5a5-428c-91b4-53afc277a1ca)


**Jenkinsfile**:  Checks out the repository, initializes Terraform with terraform init, validates the Terraform code with terraform validate, and finally applies the Terraform configuration with terraform apply to create resources.

 ![image](https://github.com/user-attachments/assets/0652e961-a440-4888-b850-88cb62c663b4)


Finally, the cluster is created on the AWS dashboard.
 

![image](https://github.com/user-attachments/assets/6abe98cf-5e38-4809-a8ca-a1913413cedc)


