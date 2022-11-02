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

Below is a Comparison between Azure App Service and  Azure Virtual Machine regarding cost, scalability, availability.
- Pricing-wise, I have run a test using a pricing calculator provided by Microsoft. In the test, I used the same configuration settings I would use on Azure for one month, and I have come to this conclusion. If I opt for Azure App Service, it would cost me nothing. Contrary, with Azure VM, it would cost me up to $13, more or less. Hence, I decided to go for Azure App Service because it's the cheapest. 

- Scalability-wise, with Azure App Service, I have the option to scale my app either 
	* horizontally (Scale-Out), add more instances of the application that runs on the App
	* vertically (Scale-up), increase memory and add more CPUs and disk space by simply changing 	the pricing tire. 
	On the other hand, Azure VM provides features for scaling, including VM scale sets, 	a group of 	identical, load-balanced VMs, and Azure VMs batch, which enables large-scale parallel and high-	performance computing (HPC) batch jobs with the ability to scale to tens, hundreds, or thousands 	of VMs. Since my application is simple and doesn't require that scalability, I decided to chose Azure 	App Service 
	
- Availability-wise, in order to have a better overview, let me show the differences between App Service and VM in Azure in terms of monthly uptime percentage. Below are two tables that show the uptime percentage of Azure App Service and Azure VM, according to SLA for App Service.

### Azure App Service 
<table>
    <thead>
        <tr>
            <th>Monthly Uptime Percentage</th>
            <th>Service Credit</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>&lt; 99.95%</td>
            <td>10%</td>
        </tr>
        <tr>
            <td>&lt; 99%</td>
            <td>25%</td>
        </tr>
        <tr>
            <td>&lt; 95%</td>
            <td>100%</td>
        </tr>
    </tbody>
</table>


### Assess app changes that would change your decision.

*Detail how the app and any other needs would have to change for you to change your decision in the last section.* 

Azure App service has some limitation that could change my decision to move to another Azure resources, such as VMs. App serves only supports a specific number of programming languages. So if happens that I needed to use a programming language that is not supported by App Service, I would have to move to an Azure Virtual Machine. 