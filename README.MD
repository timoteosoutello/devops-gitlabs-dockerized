# Usage

Taking as reference the official [doc¹](https://docs.gitlab.com/omnibus/docker/) and [doc²](https://gitlab.com/gitlab-org/omnibus-gitlab/tree/master/docker) from Gitlabs CE, is possible to start just running as docker-compose up.

# Access

Go to http://localhost:10080/ as root

# Enable gitlab runner

docker volume create gitlab-runner-config

docker run -d --name gitlab-runner --restart always -v /var/run/docker.sock:/var/run/docker.sock -v gitlab-runner-config:/etc/gitlab-runner -p 8093:8093 gitlab/gitlab-runner:latest 