## Simple BoilerPlate for new servers configuration

### Goals :

- [x] Configure needed packages
- [x] Set user's environment
- [x] secure SSH configuration
- [ ] Setup server's online security (fail2ban and so on)
- [X] Add MySQL repositery

#### Set your variables in playbooks!

In order to customize your next system, just edit the following few parameters:

* in "common_ops/tasks/main.yml" , set your timeZone
* in "common_sec/tasks/main.yml" , set your userName && SSH public key directory
* in "common_sec/tasks/main.yml" , set your custom SSH port
* in "common_sec/tasks/main.yml" , adjust your own firewall rules

As basic recommendations, RTFM DUMMY!

#### Usage :

Ready? For testing purposes, just add ```--check``` after your ```ansible-playbook``` command :

```
ansible-playbook <playbook_name.yml> --check
```
When you have checked all your desired parameters, just run the playbook by :
```
ansible-playbook <playbook_name.yml>
```

### Also..

Take a look in "group_vars" folder, You'll see that I store my credentials in a Vault file...

MAKE THE SAME! 

### Big THANKS to

* Ansible documentation!
* Qwant
* My BRAIN ==> RTFM Addict
* google

### TODO :

- [ ] fail2ban config
- [ ] Make this playbook "friendly"
