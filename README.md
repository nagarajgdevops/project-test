# assignment

#Steps to run and Important Information

1) You will require accesskey and secretkey to run the terraform. 
2) Pemfile should be present in aws before provisioning the infrastructure.
3) modify the default values of terraform ( change the pemfile name (its a must), vpc_cidr ..etc) accourding to you. 
4) jenkins machine should have git and terraform installed.
5) jenkins pipeline will fail the first time. Since i have written a declaritive pipeline, the build parameter will reload the first time and from the second time, you specify the accesskey and secretkey during a build. 
6) Modify the GIT URL in Jenkinsfile for CI/CD where you will version control the code.
7) Check the GITHUB connection on Jenkins for checkout of the source code on Jenkins workspace.

#To do ssh on private instance, i have installed ssm agents in ec2's. Just click on `Connect`  and select `Session Manager` on AWS Console and it will route you to instance terminal. 

#Once you connect to instance termainal, you can check the status of running docker containers by typing `docker ps`

#To Run the jenkins pipeline, you will need `accesskey`, `secretkey`. You can choose to `apply` or `destroy` the terraform by putting the value in `Terraform` variable.