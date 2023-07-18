#B9MG119-Assignment
###Company Choosen: Thryve Digital
![alt text](https://fresheropenings.com/wp-content/uploads/2022/09/Thryve-Digital-Off-Campus-Drive-for-2022-Batch.png)

### **INTRODUCTION**

---

Organizations started to hire larger number of technical persons as fresher and experienced candidates for their growing business needs. HR teams which are involved in the recruitment process have lot of decision-based steps, which needs to be organized effectively so the recruitment process would be seamless. For this, the team will need a to-do list, which helps them organize their day today activities. HR teams also conduct on-campus drive so the to-do list should be virtual and be accessible anytime, anywhere. Confidential information is collected as part of the process, the data entered into the application should be stored in a secure manner. Keeping everything in a personal computer or laptop is not an ideal case in this situation. So, the to-do list application should be hosted in a secure server. On-premises option is too costly which requires technical support to provision the server, internet connection and uninterrupted power supply to the server. Licenses includes operating system, Databases, and other tools also plays a vital role. Off campus drives are happening only at the end of the education year. Moving the application to cloud helps to avoid the major costs that are stated above, and once the drive is completed, we can decrease the resource usage which helps to cut down the cost.

## Benefits of cloud

---

Easy to provision
  o	There is no need to purchasing servers, required Licenses for software etc and all cloud platform providers facilitate the users within a matter of minute, to provision the system as thy needed on the go. 
Easy to scale
  o	On a Demand basis, these systems can be scaled up/down depending upon the specific requirement.
Cost Effective
  o	As we are going to pay as we use, there is no additional cost incurred.
Security
  o	On the security aspects, firewall, operating system patches and etc are handled by cloud infrastructure which increase the security without too much intervention.

![alt text](https://iamguptarishi.files.wordpress.com/2019/03/3-azure-services.png)

## **Background Of The Enterprise**

---

The company is founded in India and provides healthcare related IT services to different countries. Their primary business focus is on IT enabled services to their overseas clients. Their service offerings are Information technology health plan solutions, Information technology health customer solutions, Applications, and platform management.

### Current IT Set Up

---

The system is currently installed in an on-premises infrastructure. There are more than 500 people working on the organization. They are employing peoples who can serve healthcare related solutions to their customers. There are several cloud virtual machine technologies, Essentially, the company is creating everything in a private Virtual machine environment and have picked Azure as their cloud service provider.

## Contrast of cloud and non-cloud solutions

---

The services offered by the cloud vendor has an impact on the deployment architecture of a cloud-ready application. The choice of cloud services becomes even more crucial for an application that must operate under strict compliance and data residency requirements. Also, in cloud VPS they are using Docker images to deploy the application which helps keep the deployment effective without worrying about tools and supporting frameworks.

### Cloud

---

- Improved forecasting and management of costs
- Integrated disaster recovery and enhanced backup and restoration
- Higher saleability
- Updates to applications such as operating system and databases are automated
- Physical firewall setup and configuration
- Docker image support with server and serverless environment
- Can deploy almost any type of application without worrying about operating systems (Windows/Linux)


### Non-Cloud

---

-	Within the same data centre or in office premises
-	High levels of security and discretion requires a system administrator who is required to keep an eye on almost everything.
-	Maintenance including internet redundancy, uninterrupted power supply is a challenge.
-	Performing backups in a manual way. If it is automated using any additional software’s, then the license cost is also added with the expenses.
-	Most of the licenses cannot be leased hence we need to pay in full


### Docker support

---

Docker allows us to package our application and deliver them to cloud without any dependencies. The Docker platform allow us to run our application in an isolated environment and automatically scale up or scale down. The docker is the ideal way to deliver the application which does not have any dependencies. For example, the company can run the To-do application in a separate container under a virtual  machine which is already running an accounting software under it. Both can have their own dependency. For example, one application requires python and another one runs on .net core. 
The docker having following benefits:
- Flexible resource sharing – includes the capacity of server resources such as ram, processing power etc.
-	Scalability - When required, we can scale up or scale down a particular container.
-	Cost Effective - Running services on hardware is much cheaper than the standard servers.
-	Fast deployment - Bundle always having supporting dependencies. So, deployment is seamless.
-	Ease of migration - We can migrate the application to another location easily.
-	Better Security - Less access to work with the code running inside isolated containers. Fewer software dependencies.

## Proposed Cloud architecture

---

The proposed architecture which includes developing and maintaining application to deployment of the application. For development purposes the company uses free applications such as VS Code for code development. For better code maintenance the proposed system includes a SVN system from GitHub. GitHub act as a code repository which helps the developer to track their changes and keep the code clean and effective.
Since the company uses private virtual machines for their data security purpose, the application having docker image configuration, which is also created and maintained as part of the code repository.
For continuous development of the application and deployment, Azure dev-ops is recommended. Azure dev-ops helps compile the source code and deliver the build to the azure environment via pipelines.
For virtual machine front, Linux flavour is recommended to keep the cost low.

- Git Repository, the application uses Git as the code repository. The code repository also contains docker configuration.
- Azure DevOps - Build pipeline, the application is built on a private build pipeline. Microsoft provide free hours for building private repositories. Since the application is not going to change from time to time, free hours are enough.
- Azure Dev-ops - Release pipeline, to deliver the docker image to cloud Azure release pipeline helps.
- Docker image, the docker image configuration is part of the Git code repository. The build pipeline will build the information and prepare the docker image.
- Virtual Machine, as a part of the deployment the company created virtual machine with Linux operating system with docker support. So, the dev-ops will deploy the docker image directly to the virtual machine.
- MySQL image, MySQL instance run on docker with in the same network which helps the application to connect with the database securely.

# Final thoughts
---

Since the HR teams require extensive usage of the application for a few months in an academic year, cloud infrastructure is a cost effective and reliable implementation. Cloud deployment not only saves cost but also provides a balanced, reliable, effective and easy to grow infrastructure.
For the mentioned problem the public cloud will help use the application over the internet in a secure manner through https. The private network to connect with database as discussed in this document helps to secure the database and avoid the risk of data leakage. 
So, it is recommended to host the application in a public facing endpoint such as docker container. The database can reside on a different container which then connects with the application through a private network. 

## Advantages and disadvantages

|Advantage          |	Disadvantage |
| ------------- |:-------------:|
|Cost effectiveness on infrastructure |	Lack of control over infrastructure |
|Data can be stored across multiple geo location for disaster recovery |	Lack of control over data since it is hosted on third party cloud service |
|Server and infrastructure patches (Such as firmware updates) done by cloud infrastructure team. |	Lack of privacy and security risks |
|Multiple database and data storage options |	SLA related concerns when we are storing the data on behalf of clients |
|Ability to pay as you go and increase/decrease server performance |	Risk of having non-optimised code can be deployed on cloud which can be unidentified and unattended. |
|Server patches can be done as quick as possible | Risk of Zero-day attacks if found any|


# Conclusion

---

When comparing the cloud-based solutions with non-cloud-based solutions, the cloud-based solution is much better in terms of effectiveness, security, data redundancy and ease of deployment while keeping the cost low. Azure pricing calculator helps to forecast the cost for each month depending on the usage. This helps to keep the management aware of the expenses that comes with in it. Also, it helps to optimize our resource usage.

## Reference

Microsoft azure (https://azure.microsoft.com/)
Azure pricing calculator (https://azure.microsoft.com/en-in/pricing/calculator/)
Docker support (https://docs.docker.com/cloud/aci-integration/)
Docker Support - Microsoft (https://learn.microsoft.com/en-us/azure/app-service/tutorial-custom-container?tabs=azure-cli&pivots=container-linux)
Azure Devops - (https://azure.microsoft.com/en-in/products/devops)
Azure Devops - Docker support (https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/docker-v2?view=azure-pipelines&tabs=yaml)
