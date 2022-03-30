

## Credits
Heavily inspired by
https://github.com/aleonsan/ansible-kafka
https://github.com/sleighzy/ansible-kafka


confluents playbooks can be found here
https://github.com/confluentinc/cp-ansible/tree/7.0.1-post/playbooks

## Ansible insitallation Wsl

https://www.thomaspreischl.de/ansible-wsl-windows/

sudo apt-add-repository ppa:ansible/ansible
 sudo apt-get update
# sudo apt-get install ansible
 sudo apt install python3-pip
 sudo pip3 install pywinrm
 sudo pip3 install pyvmomi
 sudo pip3 install ansible
 sudo pip3 install ansible[azure]


 ## ssh

 ssh -i path/to/public/key.file  <user>@<ip-address>

 ## commands

 cd /etc/kafka
 /usr/bin/zookeeper-server-start  /etc/kafka/zookeeper.properties
 /usr/bin/kafka-server-start  /etc/kafka/server.properties


 ## hosts file for playsgorund
 sudo nano /etc/hosts

add entry for
127.0.0.1 zookeeper1
127.0.0.1 kafka1


 ## run playbook from wsl

 - before running unlock localhost private keystore
eval "$(ssh-agent -s)"
ssh-add ~/.ssh/<private keystore file>

 ansible-playbook main.yml -i hosts


 ## Troubleshooting

### Trouble
 When running playbook this is received
 "[WARNING]: Ansible is being run in a world writable directory <aome path>, ignoring it as an
ansible.cfg source. For more information see https://docs.ansible.com/ansible/devel/reference_appendices/config.html#cfg-in-world-        
writable-dir"

Fix with chown to limit access


## WSL Ubuntu
update
sudo apt update


upgrade
sudo apt upgrade


## Docs refernces Ansible

Command vs Shell: https://linuxhint.com/shell-vs-command-modules-ansible/#:~:text=The%20shell%20module%20executes%20commands,executes%20on%20all%20selected%20nodes.






