# infra_setup
Different playbooks and scripts to set up several OS.
The initial step to make this work is to install ansible
CentOS 8:

      yum update -y
      yum install -y epel-release
      yum install -y ansible

After installing ansible, you'll have to create a simple inventory file called *inventory* located inside */etc/ansible/* where, at least, you add *localhost* as target environment, so the content of the file will be:

    localhost
Ti run the ansible playbook you have to execute this command from the target where you clone the repo:

    ansible-playbook -v setup.yml
