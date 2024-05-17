# windows-eap-discovery
This repository is used to find out EAP process status on windows machine

# How to run eap_check.yml playbook 

First you need to create a Windows VM and also setup winrm in the machine.
After that run the following command from remote controller

```
ansible-playbook -i hosts eap_check.yml \
-e ansible_user=**** \
-e ansible_password=**** \
-e ansible_connection=winrm \
-e ansible_winrm_transport=ntlm \
-e ansible_winrm_server_cert_validation=ignore -vvv
```