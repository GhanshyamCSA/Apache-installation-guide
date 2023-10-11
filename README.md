					Apache Server
Introduction

Apache server is the most used web server application in the world and it is a crucial component in setting up a web hosting environment.apache is a very reliable and versatile server application to host a personal blog or to host a complex web application.it can be used as static web hosting, for dynamic contents and as a load balancer or as a proxy server.


Key features of Apache

These are some key features of apache http server
Open source
Scalable
Robust security features
Cross platform compatibility

In this writeup we will learn to set up the apache server in the ubuntu environment .

Step 1. Update your package lists
To ensure that you are working with the latest package list we should always update our package lists before installing any software. Although it is not mandatory but It is considered as a good practice 
![0 (2)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/95906e26-ecc3-4bcb-b29f-9d6653477dd3)


Step 2. Installing Apache
After updating our package lists we are ready to install apache. We can install it from the apt repository directly. To do this use below command
![0 (3)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/b111ae75-06f1-4494-adcd-968af789a41b)

Press y to continue. And it should install apache  in few minutes depending upon your hardware and internet speed.

Step 3. Firewall configuration
We should adjust firewall settings before testing apache. Apache registers itself with ufw during its installation. We can check the same by invoking ufw list 
![0 (4)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/ba7a493b-3ab8-4cba-b0e0-997b8cb7f342)


We can see that apache is present in ufw list.now we should provide the access from outside to default web ports
![0 (5)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/bff02699-e129-4122-8dd8-5cd37df99c85)


Now we can check the ufw status
![0 (6)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/e1b275ae-0110-4fee-aae1-004aa1996043)


*by default ufw is not active. If it is the case with you please activate ufw.

We can see that apache is now allowed in the list of ufw.

Step 4. Test your apache server

Ubuntu 22.04 starts Apache by the end of installation, by default it should be up. To make sure it is running we can check by below command
![0 (11)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/9ce1c948-44f5-4950-9f3d-13f5dad70c41)

As we can see that service is active. We can check further by requesting a page from our web server. At this point of time we haven’t set up any website to request a page so we can request the default page of apache server by entering the ip address of our web server. We can use our localhost address along with port 80 to fire up the default landing page of Apache
![0 (9)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/6cbbcde0-d9ed-407e-a6a1-2a370e395a9c)

press enter and you should get below page 
![0 (10)](https://github.com/GhanshyamCSA/Apache-installation-guide/assets/7269200/dab21976-3af6-4212-89a6-90e354dd70b2)

The result confirms that we have installed apache correctly. 

Step 5. Basic apache configuration

We can customize apache by editing apache’s configuration file.the main configuration file can be found at  /etc/apache2/apache2.conf . use ant text editor to open the file and make required changes.

Step 6. Basic management 

We have setup apache and now the server is up and running, we can use below commands to manage apache
To stop the apache service 
Sudo systemctl stop apache2

To start the service
Sudo systemctl start apache2

To restart the service 
Sudo systemctl restart apache2

To disable and re-enable at the startup
Sudo systemctl disable apache2
Sudo systemctl enable apache2



Now we have learnt how to install the apache http server and basic management of it. We are good at hosting our website or web application. 

 



.






 
