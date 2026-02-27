# vm-provision-event
Rulebook for a new VM being provisioned.

This rulebook will be fired when a provisioning event is detected. In this 
example, there is a webhook in the kickstart which tells EDA that the system
has been successfully installed. 

Then, the rulebook will check to see what the hostname is. In my lab, there
are 4 name strings which will trigger a provisoning event:
- web
- file
- app
- db

If it's a web server, the rule will:
- install httpd and mod_ssl
- start the httpd service
- enable the httpd service
- open the http and https services in the firewall

