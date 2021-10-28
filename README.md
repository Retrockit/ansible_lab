# Portable Ansible Lab

The purpose of this project is to provide a POC of a portable ansible lab via Vagrant and Virtualbox.

This lab can be utilized regardless if you're on Windows, Linux or Mac (x86_64 Macs only).

Please make sure the following is installed on your local machine:

- [Git](https://git-scm.com/downloads)

- [Vagrant](https://www.vagrantup.com/downloads)

- [Virtualbox](https://www.virtualbox.org/wiki/Downloads)

This lab will consist of three nodes:

- One Ansible Controlplane node
- Three Worker Nodes

# HOW-TO-WINDOWS

1. Make sure the preqs are installed

2. open a powershell window and type

    `git clone https://github.com/Retrockit/ansible_lab`

     `cd ansible_lab`

     `vagrant up`
3. Wait for the VMs to be created (give or take 3-5 minutes)

4. Once done type:

    `vagrant ssh controlnode`

5. Once you've remoted into the controlnode type:

    `cd ansible`

6. You're all set. When done type: 

    `exit`

7. To destroy lab type:

    `vagrant destroy -f`


# HOW-TO-LINUX/macOS(Intel)

1. Make sure the preqs are installed

2. Open a terminal window and type:


    `git clone https://github.com/Retrockit/ansible_lab`

3. Open your favorite text editor, within the ansible_lab folder you're going to open the `Vagrantfile`

5. Uncomment lines 44-45 and comment-out line 48

6. Save and exit out the file

6. Open a Terminal window and type:

    `cd ansible_lab`
    
    `vagrant up`

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


