#install ansible:
>sudo apt-get update && sudo apt-get -y upgrade && sudo apt-get -y install ansible

#Generate ssh key and upload to server /root/.ssh/id_rsa :
>ssh-keygen 
then
>copy ansible files to /etc/ansible

#Edit ssh config /etc/ssh/sshd_config
>port 1234
>PermitRootLogin prohibid-password
then
>restart service ssh

#Edit ip addr 
>/etc/ansible/hosts

#Test ansible connection 
>ansible all -m ping 

#If we have answer "pong" use:
>ansible-playbook wp.yml
