# InstallingSoftwareUsingAnsible

This is how I helped `Senior Lab Technology Manager` to install packages in all the labs using his main computer. I automated the process of installing packages using ansible playbook on around 150 computers present in my college.  
This playbook installs `namp` and `nginx` packages directly from the net and install java from the `java rpm file` downloaded by the master node by pushing it to the remote machines. 

## Instructions

1. Configure config file. `cat ~/.ansible.cfg`
3. Add the remote hosts ips in inventory file using `cat ~/inventory`
4. check `ansible all --list-hosts`
5. Edit `main.yml` according to the main.yml file.
6. Install java. `wget --no-check-certificate -c --header "Cookie: oraclelicense=accept-securebackup-cookie" https://download.oracle.com/otn-pub/java/jdk/14.0.2+12/205943a0976c4ed48cb16f1043c5c647/jdk-14.0.2_linux-x64_bin.rpm`
7. Run ansible file `ansible-playbook -i inventory main.yml`
8. ansible web -m ping
9. ansible node-1 -m shell -a 'hostname'

## References

1. https://www.techrepublic.com/article/how-to-setup-ssh-key-authentication/
2. https://www.techrepublic.com/article/how-to-install-apps-remotely-with-ansible/
3. https://docs.ansible.com/ansible/latest/modules/yum_module.html
