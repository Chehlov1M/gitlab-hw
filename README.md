# Домашнее задание к занятию «GitLab»
# Чехлов Михаил

## Задание 1
![Страница Settings → CI/CD → Runners](runner-settings.png)
*Статус раннера — active (зелёная точка), теги docker, ubuntu.*

![Вывод команды gitlab-runner list](runner-list.png)
*Раннер зарегистрирован с ID #1 (5vm1Sof3W).*

## Задание 2
![Страница Settings → CI/CD → Runners](gitlab-runner-status-and-tags-gitlab-hw.png)
*Статус раннера — active (зелёная точка), теги docker, ubuntu.*

![Вывод команды gitlab-runner list. status, git status](gitlab-runner-status-and-list-screenshot.png)
*Раннер зарегистрирован с ID #2 (2bxg3Mjny).*

![Логи задания test-pipeline](pipeline-log.png)
*Вывод команд echo, uname -a, whoami.*

Pipelines "gitlab-ci.yml".

test-docker:
  tags:
    - docker
  script:
    - echo "Running in Docker container!"
    - docker --version
    - uname -a
    - whoami
