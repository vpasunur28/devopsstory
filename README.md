

This project would deploy a web server with an index.html content as specified in html.erb file. The redirection of http to https is done inside the httpd.conf file. Self signed cert is generated through puppet code. The security groups for the instance is created using cloud formation template. EC2 instance is created using a cloud formation template. Securing the ssh access to the instance and the port configuration can be done with the above mentioned cloud formation template.

Assumption : Assuming that there is a puppet master from which we are pulling the puppet code. The EC2 instance launches with the user data to install puppet agent.


Without making any assumptions, we could also clone puppet module install puppet agent and apply the puppet module locally to have a fully functioning web server with the said html page. All of this can be done by modifying the user-date under the ec2 instance cloud formation template.





