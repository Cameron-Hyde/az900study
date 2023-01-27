# Introduction to Microsoft Azure Fundamentals #

* Microsoft Azure is a cloud computing platform that offers a wide range of services for building solutions to meet business goals.
* Azure services support everything from simple to complex, from hosting a business presence in the cloud to running fully virtualized computers managing custom software solutions.
* Azure provides services such as remote storage, database hosting, and centralized account management. It also offers new capabilities such as AI and IoT focused services.
## Upon completing this module, you will be able to:

>Define cloud computing
>Describe the shared responsibility model
>Define cloud models, including public, private, and hybrid
>Identify appropriate use cases for each cloud model
>Describe the consumption-based model
>Compare cloud pricing models.

# What is cloud computing #

* Cloud computing is the delivery of computing services over the internet.
* Computing services include common IT infrastructure such as virtual machines, storage, databases, and networking.
* Cloud computing uses the internet to deliver these services, so it is not constrained by physical infrastructure the way traditional datacenters are.
* This means that if you need to increase your IT infrastructure rapidly, you can use the cloud to rapidly expand your IT footprint instead of waiting to build a new datacenter.

# shared responsibility model #

* The shared responsibility model is a concept in cloud computing that outlines the responsibilities of the cloud provider and the consumer when it comes to maintaining and securing the cloud environment.
* The cloud provider is responsible for maintaining the physical infrastructure, including power, cooling, network connectivity, and physical security.
* The consumer is responsible for maintaining the data and information stored in the cloud, as well as access security, such as ensuring only authorized individuals and devices have access.
* Responsibility for operating systems, network controls, applications, and identity and infrastructure may depend on the specific cloud service type (IaaS, PaaS, SaaS) being used.
* IaaS places more responsibility on the consumer, while SaaS places more responsibility on the cloud provider, and PaaS is a middle ground between the two.
> You'll always be responsible for:
    >> The information and data stored in the cloud
    >> Devices that are allowed to connect to your cloud (cell phones, computers, and so on)
    >> The accounts and identities of the people, services**,** and devices within your organization

> The cloud provider is always responsible for:
    >> The physical datacenter
    >> The physical network
    >> The physical hosts

> Your service model will determine responsibility for things like:
    >> Operating systems
    >> Network controls
    >> Applications
    >> Identiy and infrastructure

# Define cloud models #

* Cloud models define the deployment type of cloud resources.The three main cloud models are: **private**, **public**, and **hybrid**.

* **Private** cloud is a cloud (delivering IT services over the internet) that’s used by a single entity, providing greater control for the company and its IT department but also greater cost and fewer benefits than public clouds.

|Organizations have complete control over resources and security       |
------------------------------------------------------------------------
|Data is not collocated with other organizations’ data                 |
------------------------------------------------------------------------
|Hardware must be purchased for startup and maintenance                |
------------------------------------------------------------------------
|Organizations are responsible for hardware maintenance and updates    |

* **Public** cloud is built, controlled, and maintained by a third-party cloud provider, it is generally available to anyone that wants to purchase cloud services.

|no capital expeditures to scale up                                    |
------------------------------------------------------------------------
|Applications can be quickly provisioned and deprovisioned             |
------------------------------------------------------------------------
|Organizations pay only for what they use                              |
------------------------------------------------------------------------
|Organizations don’t have complete control over resources and security |


* **Hybrid** cloud is a computing environment that uses both public and private clouds in an inter-connected environment, allowing for increased, temporary demand and an extra layer of security.

|Provides the most flexibility                                         |
------------------------------------------------------------------------
|Organizations determine where to run their applications               |
------------------------------------------------------------------------
|Organizations control security, compliance, or legal requirements     | 


* Multi-cloud is a scenario in which you use multiple public cloud providers.
* Azure Arc is a set of technologies that helps manage your cloud environment, whether it's a public cloud solely on Azure, a private cloud in your datacenter, a hybrid configuration, or even a multi-cloud environment.
* Azure VMware Solution lets you run your VMware workloads in Azure with seamless integration and scalability.

# Describe the consumption-based model #

* IT infrastructure models have two types of expenses: Capital expenditure (CapEx) and operational expenditure (OpEx)
* <CapEx> is a one-time, up-front expenditure to purchase or secure tangible resources
* <OpEx> is spending money on services or products over time
* Cloud computing falls under OpEx because it operates on a consumption-based model, where you pay for the IT resources you use
* This consumption-based model has benefits like no upfront costs, no need to purchase and manage costly infrastructure, ability to pay for more resources when needed and ability to stop paying for resources that are no longer needed
* With traditional datacenter, you try to estimate future resource needs, but with cloud-based model, you don't have to worry about getting resource needs just right.
* Cloud computing is the delivery of computing services over the internet by using a pay-as-you-go pricing model
* You pay only for the cloud services you use, which helps you plan and manage your operating costs, run your infrastructure more efficiently and scale as your business needs change
* Cloud computing is a way to rent compute power and storage from someone else’s datacenter, you can treat cloud resources like you would resources in your own datacenter, but when you're done using cloud resources, you give them back, you're billed only for what you use
* Cloud provider takes care of maintaining the underlying infrastructure for you, the cloud enables you to quickly solve your toughest business challenges and bring cutting-edge solutions to your users.

# Knowledge Check #
1.What is cloud computing?
>Cloud computing is the delivery of computing services over the internet.

2.Which cloud model uses some datacenters focused on providing cloud services to anyone that wants them, and some data centers that are focused on a single customer?
>The hybrid cloud model is a combination of public cloud and private cloud, using both datacenters dedicated solely to one customer and datacenters that are shared with the public.

3.According to the shared responsibility model, which cloud service type places the most responsibility on the customer?
>Infrastructure as a Service (IaaS)places the most responsibility on the consumer, with the cloud provider being responsible for the basics of physical security, power, and connectivity.