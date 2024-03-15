# DevSecOps Pipeline for a Secure & Scalable Reddit Clone on Cloud-Native Architecture


## Quick Introduction:-

Our project today is all about the specifics involved while configuring a  **DevSecOps Pipeline.**   
Ensures we're not only speeding up releases, but also being security-compliant, from the get-go.    

Technicalities in the sections that follow.

--> _What are we trying to achieve?_    
&nbsp; &nbsp; &nbsp; **Optimized QA + Speedy Delivery + Security Ingrained = Real Business Value** 

&nbsp;

### _How does the workflow actually look like?_
</br>

 > _It's more like an iterative workflow, with continuous feedback loops..._ _That's actually important when you're aiming for scalability, resilience and security._  


-  Infrastructure Provisioning through **_Terraform_**
 
- **_Elastic Kubernetes Service_** for orchestrating Containerised Applications

- **_CI/CD - Jenkins and ArgoCD_** :-    
  &nbsp; &nbsp; &nbsp; - **_Automated builds and tests_** make sure every change's verified.       
  &nbsp; &nbsp; &nbsp; - Argo CD would then facilitate **_continuous deployment_** of the application to the Kubernetes environment

- _**Security Integrations** we've made:-_       

|               | SonarQube   | Owasp     | Trivy    |
|---------------|-------------|-----------|----------|
| Static Analysis (SAST)  | ✓           | ✓         |          |
| Dependency Check       |             | ✓         |          |
| Container Image Scanning |             |           | ✓        |

-  _Deployed **Prometheus, Grafana and EFK Stack**_ (ElasticSearch, Fluentd, Kibana):-     
  &nbsp; &nbsp; &nbsp; - Configured _**Logging, Monitoring & Data Visualization**_    
 &nbsp; &nbsp; &nbsp;  - **_Real-time Insights_** into Application's health and performance.
   
</br>

> _Okay, so how does DevSecOps augment Business Processes?_

</br>

## _How does DevSecOps align with Business Objectives?_


_Simple Answer:-_   
Solid Foundation to quickly realign with changing business requirements

_It's more like a ***Strategic Enabler,*** to boost efficiency, streamline processes._    

**Quicker Product Iterations & feedback loops** through continuous integration and deployment   
--> means we're **market-agile**

</br>

> **<ins>Agile DevSecOps = Swiftly adapting to the fast-evolving business requirements.**  

</br>

Helps in both **Quality Assurance (due to Automated Testing)** &  **reducing costs due to post-deployment fixes.**  

=> Mitigating Security risks early means **averting Data Security incidents / breaches due to security lapses.**

</br>

## _Phase I : Infrastructure Setup and Tool Configuration_

> We've established the foundation for our DevSecOps Pipeline here...  

By setting up the necessary infrastructure and configuring essential tools.

**_---> VM Setup & Terraform Provisioning:_-**  

&nbsp; &nbsp; &nbsp; &nbsp; - Post provisioning a VM, we've utilized **_Terraform to automate the infrastructure setup_**.    
Terraform Files have been shared above. The EC2 instance hosting our tools has been initialized with necessary EC2 User Data.    
(Please check files above)

**--->  Tool Setup:-**      

We've installed **_Jenkins, SonarQube and Trivy_** on the provisioned VM.   
Additionally, we've configured Jenkins with the required plugins to enable seamless integration with other tools in our pipeline. 

**---> Plugin Installation + Configuration:-**   

<ins>**Purpose:-**</ins> It's essentially something that enhances the functionality of Jenkins, while allowing for seamless integration with some other tools in the Ci/CD Pipeline.   

Not going too deep into the nitty-gritties, but giving an holistic overview:-

  1- SCM Plugins:- They allow jenkins to fetch source code from Git, in our case. (Version Control Systems) for building and testing change.    
  2- Build Tools Integration Plugins:- Jenkins integrates with the build tools, through these plugins. We've used plugins for Gradle and Ant     
  3- Testing Framework Plugins:- Allows for Jenkins integrations with Testing frameworks.      
  4- Deployment and Delivery Plugins:- Plugins for deployment tools, like Docker, AWS. Allows jenkins to automate deployment to 
wide variety of environments, including staging and production.     
  5- Notification Plugins:- Jenkins notifes users about build status,  test results through plugins such plugins, We've used      
  
We've downloaded and configured the following plugins for Jenkins to enhance its functionality and enable smoother integration with our CI/CD processes.







