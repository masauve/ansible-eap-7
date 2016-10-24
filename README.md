ANSIBLE PLAYBOOK TO INSTALL JBOSS EAP AND DEPLOY APPLICATION

Prerequisites:
- Download JBOSS EAP 7.0 from Red Hat customer portal and copy the zip under the install directory
- Update the JBOSS EAP configuration in configuration/standalone.conf if requires (memory utilization and other params)
- create inventory file - only a template is provided
- Update main.yml variables for your installation (path, user and groups)
- MySQL database user, password, grants and database created

Enhancement needed:
- The unarchive command seems to copy the zip to remote everytime. Takes a long time. Need to rework

This playbook doesn't start JBOSS eap, to start go to the target machines: {{JBOSS_PATH}}/bin/standalone.sh -b 0.0.0.0
Alternately, you could modify the playbook to copy that file to init.d/jboss and enable the service
