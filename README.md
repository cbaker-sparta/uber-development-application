# Provisioning an Uber Application

__The Task__

Team 3 in Engineering-29 were tasked to provision an Uber app that uses their external API. It is built in Python using flask. The job was to create an working development, testing and production environment and to build a pipeline to move the code through them using jenkins. We started by forking the Uber App from the following repo:

https://github.com/uber/Python-Sample-Application

__The Pipeline Solution__
- The Chef tool was used to provide the solution.
- We developed a Python and Nginx cookbook to meet application dependencies which was added to the wrapper cookbook and configured application dependencies by calling a requirements.txt file.
- When the user runs ```Vagrant up``` the application starts running in dev.
- Configured Jenkins to run tests and place on the master branch.
- Packer was used to create an Amazon Machine Image (AMI) image and deploy the application on a Cloud Environment.

The above solution completes the whole CI/CD/CD pipeline. 

__How to install and use__
- Clone this repository using git clone
- Go into the named folder
- Run ```Vagrant Up```
- Go to development.local and you will see the web app. You should see the webpage below.

![](/images/uber_app_page.png)
