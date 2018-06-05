# GitLab Runner Dockerized

Configure GitLab Runner on a dockerhost.

## Requirements

### Remote host

Docker

### Deployment host

python-docker
ansible

## Role Variables

| Variable                                 | Default Value                  | Required    |
|------------------------------------------|--------------------------------|-------------|
| ansible_gitlab_runner_base_image         | gitlab/gitlab-runner:latest    |             |
| ansible_gitlab_runner_project_directory  | /srv/gitlab-runner             |             |
| ansible_gitlab_runner_container_name     | gitlab-runner                  |             |
| ansible_docker_socket_path               | /var/run/docker.sock           |             |
| ansible_gitlab_runner_docker_socket_path | {{ansible_docker_socket_path}} |             |
| ansible_gitlab_runner_executor           | docker                         |             |
| ansible_gitlab_runner_docker_image       | alpine:latest                  |             |
| ansible_gitlab_url                       | https://gitlab.com             | yes         |
| ansible_gitlab_registration_token        | PROJECT_REGISTRATION_TOKEN     |             |
| ansible_gitlab_runner_description        | docker-runner                  |             |
| ansible_gitlab_runner_tags               | [ 'docker', 'aws' ]            | recommended |
| ansible_gitlab_runner_run_untagged       | true                           |             |
| ansible_gitlab_runner_locked             | false                          |             |

## License

MIT
