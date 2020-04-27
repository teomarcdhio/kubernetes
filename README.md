# kubernetes
Basic playbook setup for a 3 nodes cluster setup. Make sure your Ansible host can access each host by coping the id_rsa.pub key in the authorized_keys file inside the .ssh folder of the root user.

Run the grantAccess to setup ansible access to each host.

Run the hostBaseCreation to setup each host with ntp, fail2ban, ufw.

Run the k8sMasterCreation and k8sWorkerCreation to install the needed kubernetes packages ( includign docker )

Run the ufwRules to allow the required ports on each host

Finally run the k8sMasterConfigCalico ( or Falnnel ) to setup the kubernetes master and

run the k8sWorkerConfig to join th workers.

Optional included a playbook to create deployment ( inclusive of service and ingress ) and the ingress config playbook to setup ingress.
