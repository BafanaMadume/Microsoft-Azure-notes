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
|Organizations don’t have complete control over resources and security|Organizations are responsible for hardware maintenance and updates|


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
  
