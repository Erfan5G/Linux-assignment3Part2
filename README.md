First, navigate to Digital Ocean and create two droplets. You can tag these droplets as you wish; in this assignment, I used the tag "web".

Before finalizing the droplet creation, utilize the Add Initialization Scripts option for configuration purposes.

Following the setup of the droplets, proceed to establish a load balancer. Once in place, verify the health of the connections between the load balancer and the servers.

Next, begin modifying server files as detailed below:

In the /var/www directory:

Add hello.conf.
Include the hello-server backend file and grant it execution permissions.
Create a directory named my-site.
Within the my-site directory, place the index.html file. This file will be served to users when they access the server.
In the /etc/systemd/system directory:

Place the hello-server.service file. This is a systemd service file for managing the server process.
In the /etc/nginx/sites-available directory:

Add the hello.conf file. Then, create a symbolic link to this file in the /etc/nginx/sites-enabled directory for Nginx to recognize and use it.


