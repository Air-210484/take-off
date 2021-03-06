## Simple BoilerPlate for new servers configuration

### Goals :

- [x] Configure needed packages
- [x] Set user's environment
- [x] secure SSH configuration
- [ ] Setup server's online security (fail2ban and so on)
- [X] Add MariaDB repository
- [ ] Setup Exim4 with Debconf
- [ ] Setup Apticron to receive server's health reports
- [ ] Use variables everywhere it is possible

#### Set your own variables in playbook!

In order to customize your next system, just set your own few parameters:

* in "base_deploy/tasks/main.yml" , set your timeZone
* in "base_custom/tasks/main.yml" , set your userName && SSH public key directory
* in "base_custom/tasks/main.yml" , set your custom SSH port
* in "base_custom/tasks/main.yml" , adjust your own firewall rules

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

In order to create a Vault file, just run :

```
ansible-vault --ask-vault-pass create <folder>/<file_name>
```

In order to edit your Vault file, just run :

```
ansible-vault --ask-vault-pass edit <folder>/<file_name>
```

### Big THANKS to

* Ansible documentation!
* Qwant
* My BRAIN ==> RTFM Addict
* google

### TODO :

- [ ] fail2ban config
