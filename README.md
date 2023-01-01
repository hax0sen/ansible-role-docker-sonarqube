ansible-role-docker-sonarqube
=========
This Ansible role installs and configures Sonarqube runnig in Docker container. 

For customize your own configuration for Sonarqube edit /templates/sonar.properties

Requirements
------------
Docker need to be pre install for this role works

Role Variables
--------------
Role variables are listed under defaults/main.yml

```yaml
# Sonarqube version
sonarqube_version: 9.8.0-community
# Sonarqube system User
sonarqube_system_user: sonarqube
# Sonarqube setup location
sonarqube_location: /home/sonarqube
# Sonarqube url
sonarqube_url: "http://localhost:9000"
# Sonarqube jdbc user
# Sonarqube jdbc url
sonarqube_jdbc_url: jdbc:postgresql://db:5432/sonar
sonarqube_jdbc_user: sonar
# Sonarqube jdbv password
sonarqube_jdbc_password: sonar
# Postgres user
postgres_user: sonar
# Postgres password¨
postgres_password: sonar
```

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters)

```yaml
- hosts: sonarqube
  roles:
    - role: ansible-role-docker-sonarqube
```

```yaml
- hosts: sonarqube
  vars:
    sonarqube_version: 9.8.0-community
    sonarqube_system_user: sonarqube
    sonarqube_url: "http://localhost:9000"
    sonarqube_jdbc_url: jdbc:postgresql://db:5432/sonar
  roles:
    - ansible-role-docker-sonarqube
```
License
-------

MIT
