# DevOpsRepo

Agile vs Devops

Agile is an iterative approach to project management and software development that focuses on collaboration, customer feedback, and rapid releases
In an agile approach, some planning and design is done upfront, but the development proceeds in small batches and involves close collaboration with stakeholders. 
Changes are incorporated continuously and a usable version of a product is often released quicker compared to products developed through the waterfall methodology. 
Agile is a collection of methodologies, not a single approach to development. It is an aggregation of scrum, extreme Programming (XP), 
and other systems of practice that developers used in years prior, and resulted from those practitioners coming together to unify these approaches into a single set of principles.

Devops is set of practices and values that combines software and IT into one , it deals with the better communication among them and deals with continuous integration 
and deployment of the services.
The goal of DevOps is to help bring together developers who write application software and operations who run the software in production. Also, 
to build and maintain the infrastructure where it runs. DevOps replaces the old approach of development teams writing applications then throwing them 
over the wall to an operations team who deploys and manages the software with minimal visibility into how it was developed. In a DevOps environment, 
developers and operations teams work side by side throughout the entire process of developing, deploying, and managing applications. 

CI, Continuous Delivery & Continuous Deployment

CI deals with maintaining your code repository in a remote service from which developers practicing continuous integration merge their changes back to the main branch as often as possible. 
The developer's changes are validated by creating a build and running automated tests against the build. 
By doing so, you avoid integration challenges that can happen when waiting for release day to merge changes into the release/master branch.

Continuous delivery is an extension of continuous integration since it automatically deploys all code changes to a testing 
and/or production environment after the build stage. 
This means that on top of automated testing, you have an automated release process and you can deploy your application any time by clicking a button.

Continuous deployment goes one step further than continuous delivery. With this practice, every change that passes 
all stages of your production pipeline is released to your customers. 
There's no human intervention, and only a failed test will prevent a new change to be deployed to production.