<!--
 Copyright (c) 2023 Ethan Shearer
 
 This software is released under the MIT License.
 https://opensource.org/licenses/MIT
-->


# Ethan Shearer | RHCE Practice Exam
###### _Use this to guage where you are, and where you need to be :)_

# Task 1
###### Configure you're ansible control node.
- Install Ansible, and any dependencies.
- Create a custom inventory file in you're home directory using the following host groups add servers to each one. `proservers` needs to be a child to `webservers`.
###### You will need to create you're own servers for this. I recommend putting two servers in each one, if not just 1 server per group.
#
```
 webservers
 devservers
 proservers
 ```
 - Use an ansible adhoc command to ping all the hosts and output the results into `ping_results.txt` in you're home directory.

# Task 2
###### Create a shell script named `repos.sh` to configure custom repositories on all managed nodes using only adhoc commands. The repository needs to be enabled and seen when listing them.
#
```
Name: examplerepo
Repo URL: http://example.com/repos/repo1
GPG File: http://example.com/repos/repo1gpg
```
- Using an ansible adhoc command, list the yum repositories and output the results into `yum_lists.txt` in you're home directory.

# Task 3
###### Create an ansible playbook named `yum_packages.yml` in you're home directory to install `mariadb, and httpd` on group `webservers`. In the same playbook install `vim` on `devservers`.

# Task 4
###### Create an ansible playbook named `create_users.yml` in you're home directory to setup users on multiple servers based on their job roles and groups. Use the provided `users.yml` in the github repository.
- Create the group `developer`, create users, and add them to that group if their job is `developer` only on inventory group `devservers`
- Create the group `webadmin`, create users, and add them to that group if their job is `webadmin` only on inventory group `webservers`
- Create the group `prodmanager`, create users, and add them to that group if their job is `prodmanager` only on inventory group `proservers`

# Task 5
###### Create an ansible playbook named `lvol.yml` in you're home directory and configure the system with the following:
#
```
Volume Group Name: my_volume_group
Logical Volume Name: my_logical_volume
Size: 1 Gigabyte
```
- Configure error handling so that if the volume group does not exist, print "Volume group does not exist."
- If the volume group does not exist, configure error handling to print "Logical volume cannot be created, volume group does not exist."

# Task 6
###### Create an ansible playbook named `html.yml` to create a custom `html.index` file using a `.j2` file and copy it to `/var/www/html/index.html` only on `webservers` group.
- The template file just needs to state the inventory hostname, and ip address of the inventory host.

# Task 7
###### Create an ansible playbook named `config.yml` in you're home directory and configure the `sshd_config` on all hosts to modify the following variables:
#
```
LoginGraceTime 1m
PermitRootLogin yes
StrictModes yes
MaxAuthTries 3
MaxSessions 5
```
# Task 8




