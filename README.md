# Provisioning an Uber Application

__The Task__

Team 3 in Engineering-29 were tasked to provision an Uber app that uses their external API. It is built in Python using flask. The job was to create an working development, testing and production environment and to build a pipeline to move the code through them using jenkins. We started by forking the Uber App from the following repo:

https://github.com/uber/Python-Sample-Application

__The Pipeline Solution__
- The Chef tool was used to provide the solution.
- Developed a Python and Nginx cookbook to meet application dependencies, built a Chef wrapper cookbook and configured dependencies such as Flask and Gunicorn. It's various modules from the python library by calling a requirements.txt file.
- When the user runs ```Vagrant Up``` the application starts running and runs in dev.
- Configured Jenkins to run tests and place on the master branch.
- Packer was used to create an Amazon Machine Image (AMI) image and deploy the application on a Cloud Environment.


__How to install and use__
- Clone this repository using git clone
- Go into the named folder
- Run ```Vagrant Up```
- Go to development.local and you will see the web app. You should see the webpage below.

![](/images/uber_app_page.png)
