

This project would deploy a web server with an index.html content as specified in html.erb file

Assumption : Assuming that there is a puppet master from which we are pulling the puppet code. The EC2 instance launches with the user data to install puppet agent.

Alternative Solution with out any assumption :

We could use git clone the puppet module, install puppet agent and apply the puppet module locally to have a fully functioning web server with the said html page. All of this can be done by modifying the user-data under the ec2 instance cloud formation template.

I have abstracted puppet module manifests by having different manifests for init, params, packages, service, config, certificate. Doing this, helps in reusing the code for various types of servers ( ex : diff env web servers - dev, qa, ct, prod ). Each can have its own cert as an example.

We can bump up the apache version just by modifying the params file than editing the whole manifest.
