#Assignment 2

				VMs vs Docker Containers

VM acts as physical computer as it uses physical resources of the underlying hardware of the computer it is running on.
VM has their own OS , also vm has full copyy of OS , application and liberaries etc
Since it uses all the resources and have its own applications, it can take up Gbs of space
VM is standalone os itself, it uses have high resource usage
There is alot to be done when running VMs since it requires set of softwares and dependencies to be installed to make the apps work
It may work on one machine and not on another due to compatibility issues on different OS

Container is abstraction layer of apps and liberaries
Containers they usualy take less space and it is isolated
Container share the kernel of the os which means multiple containers share same kernel of os and it then talk to hardware
Apps, liberaries and their dependenciew can be packaged into one conatiner
There are many containers Docker is one of them
Docker only needs to be installed and it is ready to use
It contains much less space and works same on diferent machines since it is kind of like a package
Docker container can scale very easily

				Docker Architecture

Docker has thre main components

1 - Client 
This is cli where the commands are running to run or pull the docker containers

2 - Daemon
This is the host which deals with the docker image and responsible for running images in container
cli gives commands to daemon and then it manipulates the docker image and  run them as containers
Containers are the runtime instance of an docker image
It is running on OS and communicating with OS

3- Docker Registry
It is the repository for docker images
When you pull a image it checks localy and if not found it pulls it from the registory
you can also create and push images to the registry

				Docker Commands for custom network

docker container run -d --net assignment-2 -p 9090:80 --name assignment2 nginx
docker container logs assignment2 
docker container exec -it assignment2 bash
/usr/share/nginx/html 
cat index.html

				Docker Commands for bind mounting

docker container run -v /home/osboxes/Desktop/ayaz/persist:/usr/share/nginx/html -d -p 9090:80 --name assignment2 nginx
docker container exec -it assignment2 bash
/usr/share/nginx/html 
cat > index.html
I am docker expert and this data will be persisted for the next times

#Assignment 1


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

				Benefits of Cloud Computing

Once the data is stored in the cloud, it is easier to get back-up and restore that data using the cloud.
Cloud applications improve collaboration by allowing groups of people to quickly and easily share information in the cloud via shared storage.
Cloud allows us to quickly and easily access store information anywhere, anytime in the whole world, using an internet connection. An internet cloud infrastructure increases organization productivity and efficiency by ensuring that our data is always accessible.
Cloud computing reduces both hardware and software maintenance costs for organizations.
Cloud computing allows us to easily access all cloud data via mobile.
Cloud computing offers Application Programming Interfaces (APIs) to the users for access services on the cloud and pays the charges as per the usage of service.
Cloud offers us a huge amount of storing capacity for storing our important data such as documents, images, audio, video, etc. in one place.
Data security is one of the biggest advantages of cloud computing. Cloud offers many advanced features related to security and ensures that data is securely stored and handled.

				Git vs Github

Git is a distributed peer-peer version control system. Each node in the network is a peer, storing entire repositories which can also act as a multi-node distributed back-ups. There is no specific concept of a central server although nodes can be head-less or 'bare', taking on a role similar to the central server in centralised version control systems.

Github provides access control and several collaboration features such as wikis, task management, and bug tracking and feature requests for every project.
You do not need GitHub to use Git.
GitHub (and any other local, remote or hosted system) can all be peers in the same distributed versioned repositories within a single project.

				Stages of Git
        
Untracked : We add a new file 
Staging : we add that file to staging area : git add
Local Repository: we add file to our local reposotory : git commit
Remote Repository: we add add file to our remote repository : git push/git pull
git checkout to get changes to out working repository	

				3 methods of git reset

Remove the commit from local repo, and also remove changes from staging area : Mixed
Remove the commit from local repo, but keep the les in staging area : Soft
Remove the commit from local repo, and staging area and even change the local files : Hard
