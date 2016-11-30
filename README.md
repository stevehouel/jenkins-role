# Jenkins Creation role #


## Requirements

This project must be cloned under specific project's Ansible Roles to Create Jenkins Container.

## Variables

`jenkins_path` : Jenkins Root Path for configurations and datas

`jenkins_home_path` : Jenkins Home Path (usually set to "{{ jenkins_path }}/data")

`jenkins_config_path` : Jenkins Config Path (usually set to "{{ jenkins_path }}/config")

`jenkins_docker_config_path` : Jenkins Docker daemon Config Path (usually set to "{{ jenkins_path }}/docker")

`jenkins_maven_config_path` : Jenkins Maven Settings Path (usually set to "{{ jenkins_path }}/maven")

`jenkins_port` : Listen port on Docker host to map to Jenkins container

`jenkins_master_version` : Docker Jenkins image version


## Files

* You need to create a file with path `conf-jenkins/docker2` to include the docker daemon Configurations (includes DOCKER_OPTS and Proxies).
* You need to create a folder with path `conf-jenkins/config/` to include configurations inside Jenkins. All these config files will be copied uneder /var/jenkins_home
* You need to create a file with path `conf-jenkins/settings.xml` to include Maven Configurations (Proxies etc...).
