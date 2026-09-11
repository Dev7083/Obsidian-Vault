# 🚀 DevOps (Development + Operations)

**DevOps** is a set of practices that combines **software development (Dev)** and **IT operations (Ops)** to deliver applications **faster, more reliably, and continuously**.

---

## 🔹 Why DevOps?

Traditionally:

- Developers build the software.
    
- Operations teams deploy and maintain it.
    
- This caused delays and conflicts.
    

👉 DevOps removes this gap by promoting **collaboration, automation, and continuous delivery**.

---

## 🔹 DevOps Lifecycle/Phases

![Image](https://images.openai.com/static-rsc-3/PQd169SEUwwxtQsPp8wt1GlcQitAJNh3aXwVK6ybSsp4GzDR32w6ZqH17ovewSqY4oo68RTvBr9tbsGtcpe4WNJPp_IfdvQcri0Ueqt8890?purpose=fullsize&v=1)

![Image](https://images.openai.com/static-rsc-3/1JssT43dRnj6AmZc9EbXImzBQaSLk1WhEXVOojNss6t_YgTlxYCTq3I6Db7m8irYraKbjg60ChYTiVETgOUyVSEeJcorUjJVvTpLWL4BD6Q?purpose=fullsize&v=1)

![Image](https://images.openai.com/static-rsc-3/I1q6KmhKrZQaFQkXtvRWa29tbI52CAlNZCXrQB5R_7dQfm9IRMlIguW5eJT8gy9DqloUkkViiP2jdQVI0BDgv8eA1f_4jZu_Wb5-4s-rZmk?purpose=fullsize&v=1)

![Image](https://blog.exigence.io/hubfs/298-2987566_devops-tools-clipart.png)

### Stages:

1. **Plan**
    
2. **Code**
    
3. **Build**
    
4. **Test**
    
5. **Release**
    
6. **Deploy**
    
7. **Operate**
    
8. **Monitor**
    

This cycle repeats continuously (infinity loop).

---

## 🔹 Key Concepts

- **CI (Continuous Integration)** – Automatically test and merge code.
    
- **CD (Continuous Delivery/Deployment)** – Automatically release software.
    
- **Automation** – Reduce manual work.
    
- **Monitoring** – Track system performance.
    

---

## 🔹 Popular DevOps Tools

- Git (Version Control)
    
- Jenkins / GitHub Actions (CI/CD)
    
- Docker (Containerization)
    
- Kubernetes (Container orchestration)
    
- AWS / Azure (Cloud platforms)
    

---

## 🔹 Benefits of DevOps

✅ Faster software delivery  
✅ Fewer bugs & failures  
✅ Better collaboration  
✅ Continuous improvement  
✅ Scalable & reliable systems

---

## 🔥 Simple Example (Startup Context)


Without DevOps:

- Build → Manually deploy → Errors → Downtime
    

With DevOps:

- Push code → Auto test → Auto deploy → Monitor → Fix fast
    

---

👉 In short: **DevOps helps teams build, test, and release software quickly and reliably through automation and collaboration.**

---
# 🚀 DevOps – Principles 

---

# 🔹 DevOps Principles

### 1️⃣ Collaboration

Break silos between Development and Operations teams.

### 2️⃣ Automation

Automate building, testing, deployment, and monitoring.

### 3️⃣ Continuous Integration (CI)

Frequently merge code into a shared repository and test automatically.

### 4️⃣ Continuous Delivery/Deployment (CD)

Automatically release software to production.

### 5️⃣ Monitoring & Feedback

Continuously monitor applications and gather feedback.

### 6️⃣ Infrastructure as Code (IaC)

Manage infrastructure using code (e.g., Terraform, CloudFormation).

### 7️⃣ Continuous Improvement

Regularly optimize processes and performance.

---

# 🔥 In Simple Words

DevOps = **Build fast + Test automatically + Deploy continuously + Monitor constantly**

---

# 🎯 Short Exam Summary

**DevOps is a software development approach that integrates development and operations through automation, collaboration, and continuous delivery to ensure faster and reliable software releases.**

---
# 🚀 CI/CD 

CI/CD is a DevOps practice that automates how code is built, tested, and deployed.

---

# 🔹 What is CI?

## ✅ Continuous Integration (CI)

CI means **developers frequently merge code into a shared repository**, and the system automatically:

- Builds the application
    
- Runs automated tests
    
- Detects errors early
    

### 🔁 Flow:

Developer pushes code →  
System builds →  
Runs tests →  
If tests pass → Code is accepted

### 🎯 Goal:

Catch bugs early and keep the main branch stable.

---

# 🔹 What is CD?

## ✅ Continuous Delivery

After CI, the system automatically prepares code for release.

- Code is always in a deployable state
    
- Deployment to production is manual (one click)
    

---

## ✅ Continuous Deployment

Fully automated version of delivery.

- If tests pass → Code is automatically deployed to production
    
- No manual approval needed
    

---

# 🔹 CI/CD Pipeline

![Image](https://images.openai.com/static-rsc-3/1JssT43dRnj6AmZc9EbXImzBQaSLk1WhEXVOojNss6t_YgTlxYCTq3I6Db7m8irYraKbjg60ChYTiVETgOUyVSEeJcorUjJVvTpLWL4BD6Q?purpose=fullsize&v=1)

![Image](https://developer.android.com/static/training/testing/continuous-integration/ci1.svg)

![Image](https://razorops.com/images/blog/stages-of-ci-cd-pipeline.jpg)

![Image](https://dz2cdn1.dzone.com/storage/temp/3648188-cdmaturitymodel.png)

### Typical Stages:

1️⃣ Code  
2️⃣ Build  
3️⃣ Test  
4️⃣ Release  
5️⃣ Deploy  
6️⃣ Monitor

---

# 🔥 Simple Example 

Suppose you're building an API:

Without CI/CD:

- Push code
    
- Manually test
    
- Manually deploy
    
- Errors in production
    

With CI/CD:

- Push code to GitHub
    
- GitHub Actions runs tests
    
- If tests pass → Auto deploy to server
    
- Faster, safer releases
    

---

# 🔹 Benefits of CI/CD

✅ Faster development  
✅ Early bug detection  
✅ Reduced deployment risk  
✅ Automated workflow  
✅ Reliable releases

---

# 🎯 Short Exam Definition

**CI/CD is a DevOps practice that automates the integration, testing, and deployment of code to ensure faster and reliable software delivery.**

---
# 🚀 Key Concepts of DevOps

DevOps focuses on **automation, collaboration, and continuous delivery** to improve software development and operations.

---

## 🔹 1️⃣ Collaboration

Developers and Operations teams work together instead of separately.

---

## 🔹 2️⃣ Automation

Automate building, testing, deployment, and infrastructure setup to reduce manual errors.

---

## 🔹 3️⃣ Continuous Integration (CI)

Developers frequently merge code, and automated tests verify it.

---

## 🔹 4️⃣ Continuous Delivery / Deployment (CD)

Code is automatically prepared and deployed to production.

---

## 🔹 5️⃣ Infrastructure as Code (IaC)

Infrastructure (servers, networks) is managed using code instead of manual setup.

---

## 🔹 6️⃣ Monitoring & Logging

Track system performance and detect issues quickly.

---

## 🔹 7️⃣ Version Control

Use tools like Git to manage and track code changes.

---

## 🔹 8️⃣ Microservices & Containerization

Applications are broken into small services and run in containers (like Docker) for scalability.

---

# 🔥 In Simple Words

DevOps =  
**Collaborate + Automate + Integrate + Deploy + Monitor continuously**

---

# 🎯 Short Exam Answer

**DevOps key concepts include collaboration, automation, continuous integration and delivery, infrastructure as code, monitoring, and continuous improvement to ensure faster and reliable software development.**

If you want, I can give a 5-mark or 10-mark structured answer for exams.

# 🚀 CI/CD Tools – Description

CI/CD tools automate the process of **building, testing, and deploying** applications.

---

## 🔹 1️⃣ Jenkins

- Open-source automation server
    
- Used to build, test, and deploy code
    
- Supports many plugins
    
- Highly customizable  
    ✅ Popular in enterprise environments
    

---

## 🔹 2️⃣ GitHub Actions

- Built into GitHub
    
- Automates workflows directly from repository
    
- Easy to configure using YAML files  
    ✅ Great for small to medium projects
    

---

## 🔹 3️⃣ GitLab CI/CD

- Built into GitLab
    
- Provides full DevOps lifecycle
    
- Uses `.gitlab-ci.yml` file  
    ✅ Good for integrated DevOps workflow
    

---

## 🔹 4️⃣ CircleCI

- Cloud-based CI/CD tool
    
- Fast and easy setup
    
- Good Docker support
    

---

## 🔹 5️⃣ Travis CI

- Cloud-based CI tool
    
- Integrates with GitHub
    
- Popular for open-source projects
    

---

## 🔹 6️⃣ Azure DevOps

- Microsoft’s DevOps platform
    
- Supports CI/CD pipelines
    
- Integrates well with Azure cloud
    

---

## 🔹 7️⃣ AWS CodePipeline

- Amazon’s CI/CD service
    
- Integrates with other AWS services
    
- Good for cloud-native apps
    

---

# 🔹 Supporting Tools in CI/CD

- **Docker** → Containerization
    
- **Kubernetes** → Container orchestration
    
- **SonarQube** → Code quality analysis
    
- **Nexus / Artifactory** → Artifact repository
    

---

# 🎯 Short Exam Answer

**CI/CD tools like Jenkins, GitHub Actions, GitLab CI/CD, CircleCI, and Azure DevOps automate code integration, testing, and deployment to ensure faster and reliable software delivery.**

# 🚀 CI/CD Pipeline – Description

A **CI/CD pipeline** is an automated workflow that moves code from development to production through a series of steps like build, test, and deploy.

It ensures **fast, reliable, and error-free software delivery**.

---

# 🔹 Stages of a CI/CD Pipeline

![Image](https://images.openai.com/static-rsc-3/1JssT43dRnj6AmZc9EbXImzBQaSLk1WhEXVOojNss6t_YgTlxYCTq3I6Db7m8irYraKbjg60ChYTiVETgOUyVSEeJcorUjJVvTpLWL4BD6Q?purpose=fullsize&v=1)

![Image](https://images.openai.com/static-rsc-3/iDSDaTXfVSJkPs2nGVVO8ERbiSoYjD0NroP-QSn96gibt7OVMHtyP4YaQ4MhPDqd0QsNd1KMOOo8IB64GBaZwChdmDpfsTI7Hss2EJO5s88?purpose=fullsize&v=1)

![Image](https://images.openai.com/static-rsc-3/I1q6KmhKrZQaFQkXtvRWa29tbI52CAlNZCXrQB5R_7dQfm9IRMlIguW5eJT8gy9DqloUkkViiP2jdQVI0BDgv8eA1f_4jZu_Wb5-4s-rZmk?purpose=fullsize&v=1)

![Image](https://www.researchgate.net/publication/339135798/figure/fig2/AS%3A856678622830592%401581259508160/Continuous-delivery-and-deployment.png)

## 1️⃣ Code

Developers write code and push it to a version control system (e.g., Git).

## 2️⃣ Build

The system compiles the code and creates an executable or package.

## 3️⃣ Test

Automated tests (unit, integration) are executed to check for errors.

## 4️⃣ Integrate (CI)

Code is merged into the main branch after passing tests.

## 5️⃣ Release

Application is prepared for deployment.

## 6️⃣ Deploy (CD)

The application is automatically deployed to staging or production.

## 7️⃣ Monitor

System performance and errors are continuously monitored.

---

# 🔹 How It Works (Simple Flow)

Developer pushes code →  
Pipeline runs automatically →  
Build → Test → Deploy → Monitor

If any step fails, the pipeline stops and notifies the team.

---

# 🔹 Benefits

✅ Faster releases  
✅ Early bug detection  
✅ Reduced manual work  
✅ Reliable deployments  
✅ Continuous improvement

---

# 🎯 Short Exam Definition

**A CI/CD pipeline is an automated process that integrates code changes, tests them, and deploys the application continuously to ensure fast and reliable software delivery.**

# 🚀 CI/CD as a Service

**CI/CD as a Service (CI/CDaaS)** is a **cloud-based solution** that provides Continuous Integration and Continuous Delivery tools **without installing or managing servers yourself**.

👉 The service provider hosts and manages the CI/CD infrastructure.

---

## 🔹 How It Works

1️⃣ Developer pushes code to Git repository  
2️⃣ Cloud CI/CD service automatically triggers pipeline  
3️⃣ Code is built and tested  
4️⃣ Application is deployed to cloud/server

Everything runs on the provider’s infrastructure.

---

## 🔹 Examples of CI/CD as a Service

- **GitHub Actions**
    
- **GitLab CI/CD (Cloud version)**
    
- **CircleCI**
    
- **Travis CI**
    
- **Azure DevOps (Cloud)**
    
- **AWS CodePipeline**
    

---

## 🔹 Key Features

✅ No infrastructure setup required  
✅ Scalable build environments  
✅ Easy integration with Git repositories  
✅ Automated testing & deployment  
✅ Cloud-based management

---

## 🔹 Benefits

- Faster setup
    
- Lower maintenance cost
    
- Automatic updates
    
- Easy scaling
    
- Suitable for startups & small teams
    

---

## 🔹 CI/CD as a Service vs Self-Hosted

|CI/CD as a Service|Self-Hosted CI/CD|
|---|---|
|Managed by provider|Managed by organization|
|Less setup|Full control|
|Scalable easily|More configuration effort|
|Subscription-based|Infrastructure cost|

---

# 🎯 Short Exam Definition

**CI/CD as a Service is a cloud-based solution that provides automated integration, testing, and deployment services without requiring local infrastructure management.**
# 🚀 Azure DevOps

**Azure DevOps** is a cloud-based DevOps platform by **Microsoft** that provides tools for **planning, developing, testing, and deploying** software.

It supports the complete **DevOps lifecycle**.

---

## 🔹 Main Services in Azure DevOps

![Image](https://learn.microsoft.com/en-us/azure/devops/pipelines/architectures/media/azure-devops-ci-cd-architecture.svg?view=azure-devops)

![Image](https://learn.microsoft.com/en-us/azure/devops/boards/boards/media/alm_kb_board2.png?view=azure-devops)

![Image](https://juliocasal.com/assets/images/ci-cd-pipeline.jpg)

![Image](https://learn.microsoft.com/en-us/azure/devops/pipelines/apps/cd/azure/media/data-pipeline-overview.png?view=azure-devops)

### 1️⃣ Azure Boards

- Work tracking (tasks, bugs, user stories)
    
- Supports Scrum & Kanban
    
- Sprint planning & backlog management
    

### 2️⃣ Azure Repos

- Git repositories
    
- Version control system
    
- Branching and pull requests
    

### 3️⃣ Azure Pipelines

- CI/CD pipelines
    
- Build, test, and deploy automation
    
- Supports multiple languages (Node.js, Java, .NET, Python, etc.)
    

### 4️⃣ Azure Test Plans

- Manual and automated testing
    
- Test case management
    

### 5️⃣ Azure Artifacts

- Package management (npm, Maven, NuGet, etc.)
    

---

## 🔹 Key Features

✅ Cloud-based & scalable  
✅ Integrated CI/CD  
✅ Works with GitHub and Azure Cloud  
✅ Supports Windows, Linux, macOS  
✅ Strong security & enterprise support

---

## 🔹 Benefits

- Faster development and deployment
    
- Centralized project management
    
- Better collaboration
    
- Automated testing and release
    

---

## 🔹 Simple Example (Backend Project)

If you're building a Node.js API:

- Store code in **Azure Repos**
    
- Plan tasks in **Azure Boards**
    
- Create CI/CD in **Azure Pipelines**
    
- Deploy to **Azure App Service**
    

Everything managed in one platform.

---

# 🎯 Short Exam Definition

**Azure DevOps is a Microsoft cloud platform that provides integrated tools for project planning, version control, continuous integration, testing, and deployment in the DevOps lifecycle.**

# 🚀 Continuous Deployment Pipeline in AWS

A **Continuous Deployment (CD) pipeline in AWS** automatically builds, tests, and deploys your application to production whenever code changes are pushed.

AWS provides fully managed services to implement this.

---

# 🔹 Main AWS Services Used

![Image](https://d2908q01vomqb2.cloudfront.net/fc074d501302eb2b93e2554793fcaf50b3bf7291/2022/08/05/Figure-1.-Deployment-governance-with-central-pattern-library--1024x573.png)

![Image](https://docs.aws.amazon.com/images/whitepapers/latest/cicd_for_5g_networks_on_aws/images/cicd_5g2.png)

![Image](https://docs.aws.amazon.com/images/codebuild/latest/userguide/images/arch.png)

![Image](https://d2908q01vomqb2.cloudfront.net/77de68daecd823babbb58edb1c8e14d7106e83bb/2016/12/13/Figure_2_Post_2_Stelligent_CodeBuild-1024x738.png)

### 1️⃣ AWS CodeCommit

Git-based source control repository.

### 2️⃣ AWS CodeBuild

Compiles code and runs automated tests.

### 3️⃣ AWS CodeDeploy

Deploys applications to:

- EC2
    
- Lambda
    
- ECS
    
- On-premise servers
    

### 4️⃣ AWS CodePipeline

Orchestrates the entire pipeline (automates flow).

---

# 🔹 Pipeline Stages in AWS

### 1️⃣ Source

Developer pushes code to CodeCommit or GitHub.

### 2️⃣ Build

CodeBuild compiles and tests the application.

### 3️⃣ Test

Automated tests validate functionality.

### 4️⃣ Deploy

CodeDeploy automatically deploys to production.

### 5️⃣ Monitor

Use CloudWatch to monitor performance and logs.

---

# 🔹 How It Works (Simple Flow)

Push code →  
CodePipeline triggers →  
Build & Test →  
If successful → Auto Deploy →  
Monitor application

If any stage fails, deployment stops.

---

# 🔹 Benefits

✅ Fully managed (no server maintenance)  
✅ Scalable and secure  
✅ Fast and automated deployments  
✅ Easy integration with AWS services

---

# 🔥 Example (Backend API on AWS)

If you build a Node.js API:

- Push code to GitHub
    
- CodePipeline triggers
    
- CodeBuild runs tests
    
- CodeDeploy deploys to EC2
    
- CloudWatch monitors logs
    

Fully automated production deployment.

---

# 🎯 Short Exam Definition

**A Continuous Deployment pipeline in AWS is an automated workflow using services like CodePipeline, CodeBuild, and CodeDeploy to build, test, and deploy applications automatically to production.**

# 🚀 AWS Continuous Deployment

**AWS Continuous Deployment** is the practice of automatically deploying application updates to production using AWS DevOps services whenever code changes pass testing.

It removes manual deployment steps and ensures faster, reliable releases.

---

## 🔹 Core AWS Services Used

![Image](https://docs.aws.amazon.com/images/codepipeline/latest/userguide/images/PipelineFlow.png)

![Image](https://miro.medium.com/1%2Afet9aG9Dy0REp2OJrCA3MQ.png)

![Image](https://d2908q01vomqb2.cloudfront.net/7719a1c782a1ba91c031a682a0a2f8658209adbf/2022/03/27/1-ArchitectureDiagram.png)

![Image](https://media2.dev.to/dynamic/image/width%3D800%2Cheight%3D%2Cfit%3Dscale-down%2Cgravity%3Dauto%2Cformat%3Dauto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fjglqfbaaets9ly2qsqr2.png)

### 1️⃣ AWS CodePipeline

Automates the workflow (controls stages).

### 2️⃣ AWS CodeBuild

Builds the application and runs automated tests.

### 3️⃣ AWS CodeDeploy

Deploys the application to:

- EC2
    
- ECS
    
- Lambda
    
- On-premise servers
    

### 4️⃣ Amazon CloudWatch

Monitors logs, performance, and alerts.

---

## 🔹 How AWS Continuous Deployment Works

1️⃣ Developer pushes code to GitHub/CodeCommit  
2️⃣ CodePipeline triggers automatically  
3️⃣ CodeBuild compiles & tests the code  
4️⃣ If successful → CodeDeploy deploys to production  
5️⃣ CloudWatch monitors performance

If any step fails, deployment stops.

---

## 🔹 Deployment Strategies in AWS

- **In-Place Deployment** – Updates existing servers
    
- **Blue/Green Deployment** – Switch traffic between old and new versions
    
- **Rolling Deployment** – Gradually updates instances
    

---

## 🔹 Benefits

✅ Faster releases  
✅ Reduced human errors  
✅ Automated rollback options  
✅ Scalable & secure  
✅ Seamless integration with AWS ecosystem

---

# 🎯 Short Exam Answer

**AWS Continuous Deployment is an automated process using services like CodePipeline, CodeBuild, and CodeDeploy to build, test, and deploy applications to production without manual intervention.**
