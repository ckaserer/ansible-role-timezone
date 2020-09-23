[![](https://img.shields.io/travis/com/ckaserer/ansible-role-timezone/master?style=flat-square)](https://travis-ci.com/ckaserer/ansible-role-timezone)
![gplv3](https://img.shields.io/badge/license-GPL%20v3.0-brightgreen.svg?style=flat-square)
![Maintenance](https://img.shields.io/maintenance/yes/2021?style=flat-square)

# ckaserer.timezone

The timezone role allows you to configure the timezone of your target nodes easily.

First you need to install the role on the node from which you will execute ansible via

```
ansible-galaxy install ckaserer.timezone
```

---

## Set a timezone

The playbook below sets the timezone on your current node to `Europe/Vienna`. Alternativly you can set `hosts` to a group of ansible nodes or `all`.

```
- hosts: localhost
  tasks:
    - name: "Include ckaserer.timezone"
      include_role:
        name: "ckaserer.timezone"
        apply:
          become: true
        vars:
          timezone: "Europe/Vienna"
```
