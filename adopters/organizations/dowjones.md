## Dow Jones

[Dow Jones](https://www.dowjones.com/) is a media company (Carrie TO PROVIDE MORE...)


### **Why do we use litmus**

We currently have an Istio and Kubernetes Service Mesh as our PaaS.  We understood the importance of fault tolerance on a system and transparency on microservices/ application behavior within our mesh.  This is why we wanted to ensure our deployment ecosystem is resilient by proactively simulating and identifying failures in a given environment before unplanned outages occur. Furthermore, LitmusChaos had the ability to aggregate reports, logs, and analytics from the automated chaos results.

### **How do we use litmus**

We installed the ChaosCenter in one of our meshes dedicated for our central tools and installed all the external agents with cluster scope in order to mass target k8s deployments by app label. We have all of our custom workflows by namespace living in our own ChaosHub with GitOps enabled and have cronWorkflows scheduled daily across multiple EKS integration clusters. Additionally, we have slack notifications for each application owner to review the chaos results in the ChaosCenter and Grafana dashboard.  

In the future, we plan to generate reports to send out to comms, expand this to other cluster environments (staging/ production) and fully incorporate chaos testing into our software lifecycle.

### **Benefits in using litmus**

LitmusChaos can be extended/ developed based on custom requirements, which proved very helpful when deploying litmus via helm charts.  It is well-supported and community backed up open source tool, which is incredibly helpful when integrating this into our PaaS.  Most importantly, the ability to have experiment metadata and analytics has proved helpful when troubleshooting/ identifying weaknesses.
