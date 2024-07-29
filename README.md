# Microsoft-Azure-notes

## MICROSOFT AZURE

* Cloud computing is the delivery of computing services over the internet. Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking.
* Cloud services also expand the traditional IT offerings to include things like Internet of Things (IoT), machine learning (ML), and artificial intelligence (AI).
* Because cloud computing uses the internet to deliver these services, it doesn’t have to be constrained by physical infrastructure the same way that a traditional datacenter is

### DESCRIBE THE SHARED RESPONSIBILITY MODEL

* The company is responsible for maintaining the physical space, ensuring security, and maintaining or replacing the servers if anything happens.
* The IT department is responsible for maintaining all the infrastructure and software needed to keep the datacenter up and running.
* With the shared responsibility model, these responsibilities get shared between the cloud provider and the consumer
* Physical security, power, cooling, and network connectivity are the responsibility of the cloud provider.
* The consumer isn’t collocated with the datacenter, so it wouldn’t make sense for the consumer to have any of those responsibilities.
* At the same time, the consumer is responsible for the data and information stored in the cloud. (You wouldn’t want the cloud provider to be able to read your information.) The consumer is also responsible for access security, meaning you only give access to those who need it
* Then, for some things, the responsibility depends on the situation. If you’re using a cloud SQL database, the cloud provider would be responsible for maintaining the actual database.
* With an on-premises datacenter, you’re responsible for everything. With cloud computing, those responsibilities shift.
* The shared responsibility model is heavily tied into the cloud service types (covered later in this learning path): **infrastructure as a service (IaaS)**, **platform as a service (PaaS)**, and **software as a service (SaaS)**. IaaS places the most responsibility on the consumer, with the cloud provider being responsible for the basics of physical security, power, and connectivity. On the other end of the spectrum, SaaS places most of the responsibility with the cloud provider.

![Screenshot 2024-07-24 103503](https://github.com/user-attachments/assets/90e8e409-b3dd-48fb-b194-e2ff02ee40ff)

**When using a cloud provider ,you'll always be responsible for**
- ``The information and data stored in the cloud``
- ``Devices that are allowed to connect to your cloud (cell phones, computers, and so on)``
- ``The accounts and identities of the people, services, and devices within your organization``

**The cloud Provider is always responsible for**
- ``The physical datacenter``
- ``The physical network``
- ``The physical hosts``

**Your Service Model will determine responsibility for things like**
- ``Operating systems``
- ``Network controls``
- ``Applications``
- ``Identity and infrastructure``

|Public cloud | Private cloud | Hybrid cloud |
|-------------|---------------|--------------|
|No capital expenditures to scale up|Organizations have complete control over resources and security|Provides the most flexibility|
|Applications can be quickly provisioned and deprovisioned|Data is not collocated with other organizations’ data|Organizations determine where to run their applications|
|Organizations pay only for what they use|Hardware must be purchased for startup and maintenance|Organizations control security, compliance, or legal requirements|
|Organization   s don’t have complete control over resources and security|Organizations are responsible for hardware maintenance and updates|


### Multi Cloud

* A fourth, and increasingly likely scenario is a multi-cloud scenario. In a multi-cloud scenario, you use multiple public cloud providers.
* Maybe you use different features from different cloud providers. Or maybe you started your cloud journey with one provider and are in the process of migrating to a different provider.
* in a multi-cloud environment you deal with two (or more) public cloud providers and manage resources and security in both environments.

### Azure ARC
* Azure Arc is a set of technologies that helps manage your cloud environment
* Azure Arc can help manage your cloud environment
*  whether it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid configuration, or even a multi-cloud environment running on multiple cloud providers at once.

### Azure VMware Solution 
* What if you’re already established with VMware in a private cloud environment but want to migrate to a public or hybrid cloud? Azure VMware Solution lets you run your VMware workloads in Azure with seamless integration and scalability
---

## Describe Cost Management In Azure

* Azure shifts development costs from the capital expense (CapEx) of building out and maintaining infrastructure and facilities to an operational expense (OpEx) of renting infrastructure as you need it,  whether it’s compute, storage, networking

* OpEx Cost Can be impacted by many many factors
- Resource type
- Consumption
- Maintenance
- Geography
- Subscription type
- Azure Marketplace

**RESOURCE TYPE**
* A number of factors influence the cost of Azure resources. The type of resources, the settings for the resource,
*  the Azure region will all have an impact on how much a resource costs
*  When you provision an Azure resource, Azure creates metered instances for that resource.
*  The meters track the resources' usage and generate a usage record that is used to calculate your bill.

* With a virtual machine (VM), you may have to consider licensing for the operating system or other software
* Just like with storage, provisioning the same virtual machine in different regions may result in different costs

**CONSUMPTION**
* Pay-as-you-go has been a consistent theme throughout, and that’s the cloud payment model where you pay for the resources that you use during a billing cycle
* If you use more compute this cycle, you pay more  If you use less in the current cycle, you pay less. It’s a straight forward pricing mechanism that allows for maximum flexibility.
* Azure also offers the ability to commit to using a set amount of cloud resources in advance and receiving discounts on those “reserved” resources
* Many services, including databases, compute, and storage all provide the option to commit to a level of use and receive a discount,
* When you reserve capacity, you’re committing to using and paying for a certain amount of Azure resources during a given period (typically one or three years)

## ompare the Pricing and Total Cost of Ownership calculators
* pricing calculator and the total cost of ownership (TCO) calculator are two calculators that help you understand potential Azure expenses. 
* Both calculators are accessible from the internet, and both calculators allow you to build out a configuration.

### Define Your Requirements

* For a basic web application hosted in your datacenter, you might run a configuration similar to the following.An ASP.NET web application that runs on Windows
* The web application provides information about product inventory and pricing.
*  There are two virtual machines that are connected through a central load balancer.

* The web application connects to a SQL Server database that holds inventory and pricing information.

**To Migrate to Azure One might**
* Use Azure Virtual Machines instances, similar to the virtual machines used in your datacenter.
* Use Azure Application Gateway for load balancing.
* Use Azure SQL Database to hold inventory and pricing information.

**Basic facts and requirements**
* The application is used internally. It's not accessible to customers.
* This application doesn't require a massive amount of computing power.
* The virtual machines and the database run all the time (730 hours per month).
* The network processes about 1 TB of data per month.
* The database doesn't need to be configured for high-performance workloads and requires no more than 32 GB of storage.


### DESCRIBE THE MICROSOFT COST MANAGEMENT TOOL

**What is cost Management**

* Cost Management provides the ability to quickly check Azure resource costs, create alerts based on resource spend, and create budgets that can be used to automate management of resources.
* Cost analysis is a subset of Cost Management that provides a quick visual for your Azure costs
* Using cost analysis, you can quickly view the total cost in a variety of different ways, including by billing cycle, region, resource,
* You can view aggregated costs by organization to understand where costs are accrued and to identify spending trends.
* And you can see accumulated costs over time to estimate monthly, quarterly, or even yearly cost trends against a budget.

**Cost Alerts**
* Budget alerts
* Credit alerts
* Department spending quota alerts.


#### Budget Alerts

* Budget alerts notify you when spending, based on usage or cost, reaches or exceeds the amount defined in the alert condition of the budget Cost Management budgets are created using the Azure portal or the Azure Consumption API.
* In the Azure portal, budgets are defined by cost Budgets are defined by cost or by consumption usage when using the Azure Consumption API.Budget alerts support both cost-based and usage-based budgets. Budget alerts are generated automatically whenever the budget alert conditions are met
* Whenever an alert is generated, it appears in cost alerts. An alert email is also sent to the people in the alert recipients list of the budget.

#### Credit alerts
* Credit alerts notify you when your Azure credit monetary commitments are consumed. Monetary commitments are for organizations with Enterprise Agreements (EAs).
* Credit alerts are generated automatically at 90% and at 100% of your Azure credit balance. Whenever an alert is generated, it's reflected in cost alerts, and in the email sent to the account owners.

#### Department Spending Quota alerts

* Department spending quota alerts notify you when department spending reaches a fixed threshold of the quota.


### Describe the Purpose of Tags

One way to organize related resources is to place them in their own subscriptions. You can also use resource groups to manage related resources. Resource tags are another way to organize resources.
* Tags provide extra information, or metadata, about your resources.

- **Resource management** Tags enable you to locate and act on resources that are associated with specific workloads, environments, business units, and owners.
- **Cost management and optimization Tags** enable you to group resources so that you can report on costs, allocate internal cost centers, track budgets, and forecast estimated cost.
- **Operations management Tags** enable you to group resources according to how critical their availability is to your business. This grouping helps you formulate service-level agreements (SLAs). An SLA is an uptime or performance guarantee between you and your users.
- **Security** Tags enable you to classify data by its security level, such as public or confidential.
-** Governance and regulatory compliance** Tags enable you to identify resources that align with governance or regulatory compliance requirements, such as ISO 27001. Tags can also be part of your standards enforcement efforts. For example, you might require that all resources be tagged with an owner or department name.
- **Workload optimization and automation Tags **can help you visualize all of the resources that participate in complex deployments. For example, you might tag a resource with its associated workload or application name and use software such as Azure DevOps to perform automated tasks on those resources.

* You can add, modify, or delete resource tags through Windows PowerShell, the Azure CLI, Azure Resource Manager templates, the REST API, or the Azure portal.You can use Azure Policy to enforce tagging rules and conventions.

# Describe The Core Architectural components of Azure

**What is azure**
* Azure is a continually expanding set of cloud services that help you meet current and future business challenges. Azure gives you the freedom to build, manage, and deploy applications on a massive global network using your favorite tools and frameworks.

* Azure Offers Limitless innovation. Build intelligent apps and solutions with advanced technology, tools, and services to take your business to the next level.
- **Bring ideas to life**: Build on a trusted platform to advance your organization with industry-leading AI and cloud services.
- **Seamlessly unify**: Efficiently manage all your infrastructure, data, analytics, and AI solutions across an integrated platform.
- **Innovate on trust**: Rely on trusted technology from a partner who's dedicated to security and responsibility.


## DESCRIBE AZURE MANAGEMENt INFRASTRUCTURE

* The management infrastructure includes Azure resources and resource groups, subscriptions, and accounts.

**Azure Resources and resource groups**

* A resource is the basic building block of Azure. Anything you create, provision, deploy, etc. is a resource. Virtual Machines (VMs), virtual networks, databases, cognitive services,
* Resource groups are simply groupings of resources. When you create a resource, you’re required to place it into a resource group. While a resource group can contain many resources, a single resource can only be in one resource group at a time.
*  Some resources may be moved between resource groups, but when you move a resource to a new group, it will no longer be associated with the former group.
*  Resource groups provide a convenient way to group resources together.. When you apply an action to a resource group, that action will apply to all the resources within the resource group.If you delete a resource group, all the resources will be deleted.

#### AZURE SUBSCRIPTIONS

* A subscription provides you with authenticated and authorized access to Azure products and services,An Azure subscription links to an Azure account, which is an identity in Microsoft Entra ID or in a directory that Microsoft Entra ID trusts.

 There are **two types of subscription**boundaries that you can use:

 * **Billing boundary**: This subscription type determines how an Azure account is billed for using Azure. You can create multiple subscriptions for different types of billing requirements. Azure generates separate billing reports and invoices for each subscription so that you can organize and manage.costs.
 * **Access control boundary**: Azure applies access-management policies at the subscription level, and you can create separate subscriptions to reflect different organizational structures. An example is that within a business, you have different departments to which you apply distinct Azure subscription policies. This billing model allows you to manage and control access to the resources that users provision with specific subscriptions.

---
---

## MICROSOFT AZUZE DATA FUNDAMENTALS: EXPLORE CORE DATA CONCEPTS
* Data is the foundation on which all software is built. By learning about common data formats, workloads, roles, and services,
* You can classify data as structured, semi-structured, or unstructured.

### STRUCTURED DATA
* Structured data is data that adheres to a fixed schema, so all of the data has the same fields or properties. Most commonly, the schema for structured data entities is tabular , the data is represented in one or more tables that consist of rows to represent each instance of a data entity, and columns to represent attributes of the entity
* Structured data is often stored in a database in which multiple tables can reference one another by using key values in a relational model;

### SEMI-STRUCTURED DATA
* Semi-structured data is information that has some structure, but which allows for some variation between entity instances. One common format for semi-structured data is JavaScript Object Notation (JSON).

### UNSTRUCTURED DATA
* Not all data is structured or even semi-structured. For example, documents, images, audio and video data, and binary files might not have a specific structure. This kind of data is referred to as unstructured data.
