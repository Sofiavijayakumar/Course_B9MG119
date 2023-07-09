#B9MG119-Assignment
###Company Choosen: Thryve Digital
![alt text](https://fresheropenings.com/wp-content/uploads/2022/09/Thryve-Digital-Off-Campus-Drive-for-2022-Batch.png)

### **INTRODUCTION**

---

Business right now started to hire larger number of technical persons as fresher and experience candidates. HR team having lots of works which needs to be organized effectively so the recruitment process would be seamless. For this, the team looking for a to-do list which help them to organize their day today job. HR team also conduct on-campus drive so the to-do list should not only be in their local machine. It should be reached from anywhere when HR team requires. Since the recruitment process having lots of confidential information, the whatever data entered with in the application should store in secured manner. Keeping everything in a personal computer or laptop is not an idle case in this requirement. So, the to-do application should hosted in a secured server. On-premises option is too costly which require a technical person support to provision the server, internet connection, uninterrupted power supply to server. Licenses includes operating system, Databases, and other tools also plays a vital role. Off campus drives are happening only at the education year end. Moving the application to cloud helps to avoid the major cost which stated above and also once drive completed, we can decrease the resource usage which helps to cut down the cost.

## Benefits of cloud

---

-Easy to provision - We no need to worry about purchase servers, required Licenses for software’s and etc. All can be done in matter of minute.
-Easy to scale - When require the system can be scaled up/down depends upon the specific requirement.
-Cost Effective - We are going to pay as we use. So no additional cost incurred.
-Security - On security aspects, firewall, operating system patches and etc handled by cloud infrastructure which increase the security without much intervention.

![alt text](https://iamguptarishi.files.wordpress.com/2019/03/3-azure-services.png)

## **Background Of The Enterprise**

---

The company is founded in India and providing healthcare related IT services to different countries. Their primary focus is on IT enabled services to their overseas clients. They are offering services included Information technology health plan solutions, Information technology health customer solutions, Applications and platform management.

### Current IT Set Up

---

The system is currently installed in an on-premises infrastructure. There are more than 500 people working on the organization. They are employing peoples who can serve healthcare related solutions to their customers. There are certain cloud virtual machine technologies. Essentially, They are creating everything in a private Virtual machine environment and have picked Azure as their cloud service provider.

## Contrast of cloud and non-cloud solutions

---

The services offered by the cloud vendor always have an impact on the deployment architecture of a cloud-ready application. The choice of cloud services becomes even more crucial for an application that must operate under strict compliance and data residency requirements. Also in cloud VPS they are using Docker images to deploy the application which helps to keep the application deployment in an effective manner without worrying about tools and supporting frameworks.

### Cloud

---

- Improved forecasting and management of costs.
- Integrated disaster recovery and enhanced backup and restoration.
- Higher saleability.
- Updates to applications such as operating system, databases are automated.
- Physical firewall setup and configuration.
- Docker image support with server and serverless environment.
- Can deploy almost any type of application without worrying about operating systems (Windows/Linux).

### Non-Cloud

---

- Within the same data centre or in office premises.
- High levels of security and discretion. Require system administrator who requires to keep an eye on almost everything.
- Maintenance including internet redundancy, uninterrupted power supply is challenging.
- Performing the backups in manual way. If it automated using any additional software’s, then the license cost also added with expenses.
- Most of the license can not be leased hence we need to pay full money.

### Docker support

---

Docker allows us to package our application and deliver them to cloud without any dependencies. The Docker platform allow us to run our application in an isolated environment and allow us to automatically scale up or scale down. The docker is idle way to deliver application which does not having dependency. For example the company can able to run the Todo application in a separate container under virtual machine which already running a accounting software under it as separate container. Both can have their own dependency. For example one application requires python and another one runs on .net core. The docker having following benefits

- Flexible resource sharing - includes capacity of server resources such as ram, processing power and etc
- Scalability - When requires we can scale up or scale down a particular container.
- Cost Effective - Running services on hardware is much cheaper than standard server.
- Fast deployment - Bundle always having supporting dependencies. So deployment is seemless.
- Easy of migration - We can migrate the application to another location easily.
- Better Security - Less access to work with the code running inside containers. Fewer software dependencies.

## Cloud architecture deployment proposed

---

The proposed architecture which includes from developing, maintaining application to deployment of the application . For development purpose the company use free applications such as VS Code for code development. For better code maintenance the proposed system includes a SVN system from Github. Github act as code repository which helps developer to track their changes and keep the code clean and effective.

Since the company uses private virtual machines for their data security purpose, the application also having docker image configuration, which also created and maintained as part of code repository.

For continuous development of the application and deployment, Azure dev-ops recommended. Azure dev-ops helps to compile the source code and deliver the build to the azure environment via pipelines.

For virtual machine front, Linux flavour recommended to keep the cost low.

- Git Repository - The application uses Git for code repository. The code repository also contains docker configuration.
- Azure DevOps - Build pipeline - The application build via private build pipeline. Microsoft provide free hours for building private repositories. Since the application not going to change time to time, free hours are enough.
- Azure Dev-ops - Release pipeline - To deliver the docker image to cloud Azure release pipeline helps.
- Docker image - The docker image configuration is part of Git code repository. The build pipeline will build the information and prepare the docker image.
- Virtual Machine - As a part of deployment the company created virtual machine with Linux operating system with docker support. So the dev-ops will deploy the docker image directly to the virtual machine.
- MySQL image - My SQL instance run on docker with in same network which helps application to connect with database securely.

# Conclusion

---

When comparing the cloud based solution with non-cloud based solution, the cloud based solution is much better in terms of effectiveness, security, data redundancy, ease of deployment at the same time keeping the cost low. Azure pricing calculator helps to forecast the cost for each month depends upon the usage. This helps to keep management aware of the expenses comes with in their budget. Also, it helps to optimize our resource usage.

## Reference

Microsoft azure (https://azure.microsoft.com/)
Azure pricing calculator (https://azure.microsoft.com/en-in/pricing/calculator/)
Docker support (https://docs.docker.com/cloud/aci-integration/)
Docker Support - Microsoft (https://learn.microsoft.com/en-us/azure/app-service/tutorial-custom-container?tabs=azure-cli&pivots=container-linux)
Azure Devops - (https://azure.microsoft.com/en-in/products/devops)
Azure Devops - Docker support (https://learn.microsoft.com/en-us/azure/devops/pipelines/tasks/reference/docker-v2?view=azure-pipelines&tabs=yaml)
