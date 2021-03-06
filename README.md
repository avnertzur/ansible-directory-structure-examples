Ansible Directory Structure Examples
====================================

*Goal:*

- Install Apache2 on Ubuntu and 
- Disable the default website and 
- Restart Apache2

*Different methods to achieve the above goal:*

1. Basic Ansible Playbook
2. Basic Roles
3. Basic Roles with Multi Environment Setup
4. Advanced - Shared Global Roles with multiple Playbooks

Basic Ansible Playbook
---------------------

To run in a local computer:

```
  cd basic
  vagrant up
```

Using Inventory file:

```
  ansible-playbook site.yml -i inventory
```

Using Command line parameters:

```
  ansible-playbook site.yml \
  -i 10.0.0.200, \
  -u vagrant \
  --private-key ./.vagrant/machines/default/virtualbox/private_key
```

Basic Roles
---------------------

To run in a local computer:

```
  cd basic-roles
  vagrant up
  ansible-playbook site.yml -i inventory
```

Basic Roles with Multi Environment Setup
---------------------------------------

To run in a local computer:

```
  cd basic-roles-multi-environment
  vagrant up
```

To run in Development Environment mode:

```
  ansible-playbook site.yml -i inventories/development
```

To run in Staging Environment mode:

```
  ansible-playbook site.yml -i inventories/staging
```

To run in Production Environment mode:

```
  ansible-playbook site.yml -i inventories/production
```

Advanced - Shared Global Roles with multiple Playbooks
------------------------------------------------------

To run in a local computer:

```
  cd advanced-shared-global-roles
  vagrant up
  ansible-playbook site.yml -i inventories/development
```

