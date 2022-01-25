# Portable Ansible Lab

The purpose of this project is to provide a POC of a portable ansible lab via Vagrant and Virtualbox.

This lab can be utilized regardless if you're on Windows or Linux.

Please make sure the following is installed on your local machine:

- [Git](https://git-scm.com/downloads)

- [Vagrant](https://www.vagrantup.com/downloads)

- [VirtualBox](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html#vbox)

- [VirtualBox Extension Pack](https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html#extpack)

This lab will consist of four nodes:

- One Ansible Controlplane node
- Three Worker Nodes

# HOW-TO-WINDOWS

1. Make sure the prerequisites are installed

2. open a powershell window and type

    `git clone https://github.com/Retrockit/ansible_lab`

     `cd ansible_lab\Windows`

3. type: `rm id_rsa*` to delete the reference keys. You're going to generate your own keys.

        a. In the same powershell window type: ssh-keygen

        b. When prompted to name keys type: id_rsa

        c. your id_rsa and id_rsa.pub keys will be saved to the current directory
        
4. type: `vagrant up`


4. Wait about 3-5 minutes for the VMs to be create
    (NOTE: You will prompted once to enter credentials to mount the SMB share. Make sure to enter your windows username and password correctly.)

4. Once done type:

    `vagrant ssh controlnode`



5. Once you've remoted into the controlnode type:

    `cd ansible`

    This will take you into the ansible folder with all that you need to try out ansible: 
    
    - ansible.cfg pointing to hosts.ini inventory file 
    
    - hosts.ini with all the vagrant machines

    - blank playbook.yml

6. You're all set. When done type: 

    `exit`

7. To destroy lab type:

    `vagrant destroy -f`



# HOW-TO-LINUX

1. Make sure the prerequisites are installed

2. Open a terminal window and type:


    `git clone https://github.com/Retrockit/ansible_lab`


6. Open a Terminal window and type:

    `cd ansible_lab/Linux`

7. type: `rm id_rsa*` to delete the reference keys. You're going to generate your own keys.

        a. In terminal type: ssh-keygen

        b. name the keys: id_rsa

        c. Press Enter twice to save the public and private keys to the current directory

5. type: `vagrant up`

3. Wait for the VMs to be created (give or take 3-5 minutes)

4. Once done type:

    `vagrant ssh controlnode`

5. Once you've remoted into the controlnode type:

    `cd ansible`

    This will take you into the ansible folder with all that you need to try out ansible: 
    
    - ansible.cfg pointing to hosts.ini inventory file 
    
    - hosts.ini with all the vagrant machines

    - blank playbook.yml

6. You're all set. When done type: 

    `exit`

7. To destroy lab type:

    `vagrant destroy -f`


