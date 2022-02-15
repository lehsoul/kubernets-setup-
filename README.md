# kubernets-setup

To orchestrate and manage resources efficiently, the suite uses Kubernetes as the platform to provide a reliable approach to scheduling resources and empower the application to be more fault-tolerant. Cloud-native Kubernetes platforms make the provisioning and management of Kubernetes much easier. With the cloud-native Kubernetes, the suite can serve customers in a secure, resilient, and simple way.On AWS, the cloud-native Kubernetes solution is Amazon Elastic Kubernetes Service (EKS)
# SMA service management Automation X suite need to deploy on AWS prod tenant
# Components
SMA: the suite product shipped and running in the form of containers and managed by Kubernetes.
Kubernetes: open-source software that allows you to deploy and manage containerized applications at scale.
Public subnet: a public subnet is for external-facing resources such as load balancers, bastion nodes, and NAT gateway.
Private subnet: a private subnet is for internal-facing resources such as EKS worker nodes, databases, and storage.
Bastion node: a node that sits in a public subnet. It's used to connect to resources in a private subnet such as Kubernetes, databases, and storage to perform deployment, persistent volume setup, database setup, upgrade, troubleshooting, and other operational tasks.
Elastic Kubernetes Service (EKS): a fully managed service provided by AWS. Once it's provisioned, the following services are ready to work as a Kubernetes platform for you:
Control Plane: manages when and where containers are started on your cluster and monitors their status.
Worker Nodes (Group): nodes to run your containers. The worker nodes are deployed across multiple AWS availability zones for high availability and fault tolerance.
Elastic File Service (EFS): a managed NFS service that stores data used by the containerized applications in Kubernetes (such as search engine storage, attachments, certificates, and logs). The storage is called Persistent Volume (PV) in Kubernetes.
Relational Database Service (RDS): a database service that stores transactional data and metadata used by the containerized applications in Kubernetes.
Elastic Container Registry (ECR): a managed Docker registry service that's secure, scalable, and reliable. The suite applications are shipped as container images, which are stored in an ECR.
Load balancer: used to route traffic from external applications to internal applications deployed on Kubernetes. Load balancers triggered from the Kubernetes service are able to discover the backend worker node change and always fit the latest status of the worker node pool.
NAT gateway: enables instances in a private subnet to connect to the Internet or other AWS services, but prevents the Internet from initiating a connection with those instances.

