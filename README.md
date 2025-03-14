**Jenkins on AWS EC2 Setup and Configuration**
 - This repository contains step-by-step instructions for setting up Jenkins on an AWS EC2 instance, creating a freestyle project with a simple shell command, installing the Role-Based Authorization Plugin, and managing users and roles.
 - Check attached screenshots for all the steps below as reference.

**Steps to Launch Jenkins on AWS EC2**
 - Log in to your AWS Management Console.
 - Navigate to the EC2 Dashboard and click Launch Instance.
 - Choose an Amazon Machine Image (AMI), such as Amazon Linux 2 or Ubuntu.
 - Select an instance type (e.g., t2.micro) and configure the instance details.
 - Add a security group rule to allow inbound traffic on port 8080 (Jenkins) and port 22 (SSH).

**Install Java and Jenkins**
 - https://www.jenkins.io/doc/book/installing/

**Access Jenkins**
 - Open a browser and navigate to: http://<public-ip-address>:8080
 - Complete the Jenkins setup by installing suggested plugins and creating an admin user.

**Installing the Role-Based Authorization Plugin**
 - Navigate to Manage Jenkins > Manage Plugins .
 - Go to the Available tab and search for Role-Based Authorization Strategy .
 - Install the plugin and restart Jenkins if prompted.

**Creating Users and Assigning Roles**
 - Enable Role-Based Authorization
 - Navigate to Manage Jenkins > Configure Global Security .
 - Under Authorization , select Role-Based Strategy .
 - Save the configuration.
 - **Create Roles**
 - Navigate to Manage Jenkins > Manage and Assign Roles > Manage Roles .
 - Under Global roles , create the following roles:
 - admin: Assign all permissions. dev: Assign permissions like Job Read, Job Build, etc.
 - **Create Users**
 - Navigate to Manage Jenkins > Manage Users > Create User .
 - Create two users: John Doe & Jane Doe
 - Assign Roles to Users: Navigate to Manage Jenkins > Manage and Assign Roles > Assign Roles .

**Creating a Freestyle Project**
 - Log in to Jenkins and click New Item.
 - Enter a name for the job (e.g., Sample-Freestyle-Job) and select Freestyle project.
 - Under the Build section, click Add build step and select Execute shell.

   **Conclusion**
   - You have successfully:
Launched Jenkins on an AWS EC2 instance.
Created a freestyle project with a simple shell command.
Installed the Role-Based Authorization Plugin.
Created users and assigned roles
