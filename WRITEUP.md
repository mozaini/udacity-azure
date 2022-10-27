# Write-up 
## Deploy an Article CMS to Azure App Service 

### Analyze, choose, and justify the appropriate resource option for deploying the app.

*For **both** a VM or App Service solution for the CMS app:*
- *Analyze costs, scalability, availability, and workflow*
- *Choose the appropriate solution (VM or App Service) for deploying the app*
- *Justify your choice*

before I chose which compute service I should opt for, I looked at their descriptions. According to Microsoft, Azure App Service is "A managed service for hosting web apps, mobile app back ends, RESTful APIs, or automated business processes", and Azure Virtual Machine is  "software emulation of physical computer. They include a virtual processor, memory, storage, and networking resources. VMs host an operating system, and you can install and run software just like a physical computer" 

With VMs, you can create and use VMs in the cloud. Virtual Machines provides infrastructure as a service (IaaS) and can be used in different ways. When you need total control over an operating system and environment, VMs are an ideal choice.

On the other hand, With Azure App Service, you can quickly build, deploy, and scale enterprise-grade web, mobile, and API apps running on any platform. You can meet rigorous performance, scalability, security, and compliance requirements while using a fully managed platform to perform infrastructure maintenance.

Based on the above descriptions of both Azure resources, I do not need an entire infrastructure to build and deploy my app. Instated, I just need an app service to implement my project. Azure app Services provide all capabilities and scalabilities requirements needed for this project. In additional, Azure App Service provides a free tier plan which is sufficient to deploy my app without the need to use a total infrastructure. Also, with Azure App Service, I would be able to scale the resources I need both vertically and horizontally, meaning I can adjust the amount of RAM or CPUs, for example, as needed. Lastly, deploying an app is very straightforward on App Service, for example, I can deploy my app from GitHub. 

Therefore, I choose to deploy the Article CMS app on Azure App Service.

### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

Azure App service has some limitation that could change my decision to move to another Azure resources, such as VMs. App serves only supports a specific number of programming languages. So if happens that I needed to use a programming language that is not supported by App Service, I would have to move to an Azure Virtual Machine. 