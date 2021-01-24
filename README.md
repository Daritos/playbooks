# Ansible playbooks

This is a repository crafted to hold useful playbooks and roles to simply the setup and configure applications and services that I commonly utilize.

## Get started (Ubuntu 20.04)

Install ansbile

```bash
sudo apt update
sudo apt install ansible -y
```

### Setup inventory

Create your inventory file

#### Inventory examples

##### Single node (local connection)

Create an INI formated file

```bash
editor ./inventory.ini
```

Containing

```ini
node1 ansible_connection=local local_release_dir={{ansible_env.HOME}}/releases
```

##### Multiple nodes

Create a YAML formated file

```bash
editor ./inventory.yml
```

Containing

```yaml
all:
  node1:
    ansible_host: 127.0.0.1
```

### Run a playbook

Execute the following command

```bash
ansible-playbook -i <PATH_TO_INVETORY> <PATH_TO_PLAYBOOK>
```

References / good reads:

- <https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-ansible-on-ubuntu-20-04>

