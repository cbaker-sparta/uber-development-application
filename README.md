# Provisioning an Uber Application

__The Task__
Team 3 in Engneering-29 were tasked to provision an Uber app built with Python that uses their external API. It is built in Python using flask. The job was to create an working development, testing and production environment and to build a pipeline to move the code through them using jenkins. We started by cloning the Uber App from the following repo:

https://github.com/uber/Python-Sample-Application

__The Pipeline Solution__
- A solution was created using Chef which is a configuration tool and allows the software to be spun up multiple times in different locations.
- Developed a Python and Nginx cookbook to meet dependencies
- Built a Chef wrapper cookbook and configured
 dependencies of the Application which included Python 2.7 and an Nginx web server and various modules from the python library.
- Created an Nginx Reverse Proxy server provision Nginx as a reverse proxy and have it proxy port 80 to the port of your application. The application port should be configurable using chef attributes but default to 3000.
- Configured Jenkins to run tests
- User Packer to create an AMI image it order to achieve Continuous Deployment.


__How to install and use__
- Clone this repository using git clone
- Go into the named folder
- Run ```Vagrant Up```
- Go to development.local and you will see the web app. You should see the webpage below.

![](/images/uber_app_page.png)
