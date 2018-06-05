GitLab Runner Dockerized
=========

Configure GitLab Runner on a dockerhost.

Requirements
------------

Docker on the remote host has to be already installed.  
Ansible has to be able to execute docker related tasks, so all ansible dependencies related to docker have to be installed.

Role Variables
--------------

|Variable|Default Value|
|ansible_gitlab_runner_base_image| 'gitlab/gitlab-runner:latest'|
|ansible_gitlab_runner_project_directory| '/srv/gitlab-runner'|
|ansible_gitlab_runner_container_name| 'gitlab-runner'|
|ansible_docker_socket_path| '/var/run/docker.sock'|
|ansible_gitlab_runner_docker_socket_path| '{{ ansible_docker_socket_path }}'|

License
-------

MIT
