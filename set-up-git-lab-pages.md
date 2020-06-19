# Cài đặt GitLab chạy trên linux container

## Chuẩn bị
## Cài đặt Gitlab
sestatus
1. Add this line to your Jekyll site’s Gemfile:

    ```
    sudo docker run --detach \
      --hostname phong.test \
      --publish 443:443 --publish 80:80 \
      --name gitlab \
      --restart always \
      --volume $GITLAB_HOME/config:/etc/gitlab \
      --volume $GITLAB_HOME/logs:/var/log/gitlab \
      --volume $GITLAB_HOME/data:/var/opt/gitlab \
      gitlab/gitlab-ce:latest
    ```
## Cài đặt Gitlab runner
