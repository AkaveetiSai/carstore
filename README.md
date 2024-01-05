# Architecture Description

![assets_-LgLv25e2BrxRC5m6flh_-LiRaWYeeyfVw0UcP6N1_-LiReuowSS1wOL09A5fI_code deploy](https://github.com/AkaveetiSai/carstore/assets/74001902/56769025-ee58-4e39-a714-3afc0be6c067)


The image depicts a simplified architecture of a deployment pipeline, but it doesn't provide detailed architectural elements or structures typically associated with building or infrastructure design. Therefore, I need to focus on the components and flow represented in the diagram.

The first component in this architecture is "Dev Teams," represented by a gear icon. Dev Teams are responsible for developing software and pushing their code to GitHub, as indicated by the arrow labeled "Push." GitHub is a platform where developers store and manage their code repositories. In this architecture, any push to GitHub triggers an automated process.

The second component is "GitHub," denoted by its iconic logo. When code is pushed to GitHub, it triggers AWS CodeDeploy - illustrated by an arrow labeled "Trigger." AWS CodeDeploy automates code deployments to any instance, including Amazon EC2 instances and on-premises servers. This automation helps minimize downtime during application deployment.

The third component is "AWS CodeDeploy," represented by its green logo. AWS CodeDeploy is a service that coordinates application deployments across multiple Amazon EC2 instances. It allows developers to specify deployment configurations, such as the type and number of instances, the deployment order, and the rollback options. AWS CodeDeploy also provides feedback on the status and outcome of each deployment.

The fourth and final component is "Amazon EC2," denoted by its orange logo. Amazon EC2 (Elastic Compute Cloud) is a web service that provides resizable compute capacity in the cloud. It enables developers to launch and manage virtual servers, called instances, that run applications. Amazon EC2 offers various options for instance types, operating systems, storage, networking, and security.

- The diagram shows a linear flow from development teams pushing code to deployment on EC2 instances.
- Dev Teams use gears symbol indicating engineering or development work.
- GitHub is used as the version control system where codes are stored.
- A push action triggers AWS CodeDeploy for automated deployment.
- AWS CodeDeploy is represented with its green logo.
- Deployment process flows towards Amazon EC2 instances.
- EC2 (Elastic Compute Cloud) provides resizable compute capacity in the cloud.
- Arrows indicate the direction of workflow from left (development) to right (deployment).
- The word “Trigger” indicates an automated response following a push action to GitHub.
- “Deploy” signifies the action of implementing code onto EC2 instances via AWS CodeDeploy.




# AWS CICD Pipeline Code Deployment to AWS EC2 Instance


<b>User Data for Dependencies installations for AMAZON Linux 2:-</b>

#!/bin/bash<br />
sudo yum -y update<br />
sudo yum -y install ruby<br />
sudo yum -y install wget<br />
cd /home/ec2-user<br />
wget https://aws-codedeploy-ap-south-1.s3.ap-south-1.amazonaws.com/latest/install<br />
sudo chmod +x ./install<br />
sudo ./install auto<br />
sudo yum install -y python-pip<br />
sudo pip install awscli<br />


