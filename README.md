# GitLab Runner Dockerized

Configure GitLab Runner on a dockerhost.
Active development is done at https://chaos.expert/agowa338-ansible/ansible-gitlab-runner-dockerized
GitHub is automatically updated by GitLab and Ansible Galaxy automatically pulls from GitHub.

## Requirements

### Remote host

Docker

### Deployment host

python-docker
ansible

## Role Variables

| Variable                                   | Default Value                             | Required    |
|--------------------------------------------|-------------------------------------------|-------------|
| ansible_gitlab_runner_base_image           | gitlab/gitlab-runner:latest               |             |
| ansible_gitlab_runner_project_directory    | /srv/gitlab-runner                        |             |
| ansible_gitlab_runner_container_name       | gitlab-runner                             |             |
| ansible_docker_socket_path                 | /var/run/docker.sock                      |             |
| ansible_gitlab_runner_docker_socket_path   | {{ansible_docker_socket_path}}            |             |
| ansible_gitlab_runner.name                 | gitlab-runner                             |             |
| ansible_gitlab_runner.description          | gitlab-runner on {{ inventory_hostname }} |             |
| ansible_gitlab_runner.executor             | [ "docker" ]                              |             |
| ansible_gitlab_runner.tags                 | [ "docker" ]                              |             |
| ansible_gitlab_runner.run_untagged         | True                                      |             |
| ansible_gitlab_runner.locked               | False                                     |             |
| ansible_gitlab_runner.check_interval       | 0                                         |             |
| ansible_gitlab_runner.maximum_timeout      | 600                                       |             |
| ansible_gitlab_runner.docker.image         | alpine:latest                             |             |
| ansible_gitlab_runner.docker.tls_verify    | True                                      |             |
| ansible_gitlab_runner.docker.privileged    | False                                     |             |
| ansible_gitlab_runner.docker.disable_cache | False                                     |             |
| ansible_gitlab_runner.docker.shm_size      | 0                                         |             |
| ansible_gitlab_url                         | https://chaos.expert                      |             |
| ansible_gitlab_registration_repossitories  |                                           | yes         |
| ansible_gitlab_api_token                   |                                           | yes         |
| gitlab_runner__runners_api_url             | {{ ansible_gitlab_url }}/api/v4/runners   |             |
| gitlab_runner__projects_api_url            | {{ ansible_gitlab_url }}/api/v4/projects  |             |

## License

MIT
