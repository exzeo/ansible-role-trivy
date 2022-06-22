Ansible Role trivy
=========

Installs Helm Command Line on Debian/Ubuntu servers. 
Releases: https://github.com/aquasecurity/trivy/releases

Role Variables
--------------

```
# Version of 'trivy' to install, defaults to latest version
trivy_version: ""

# Toggling this will uninstall from the server
uninstall: false
```


Example Playbooks
----------------

Minimal:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.trivy
```

Specific Version:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.trivy
      vars:
        trivy_version: "0.27.1"
```

Uninstall:
```
- name: Install CLI
  hosts: all
  roles:
    - role: exzeo.trivy
      vars:
        uninstall: true
```