# docker-monitoring (cadvisor)

Плейбук для установки cadvisor на хост с Docker'ом для мониторинга контейнеров.

В качестве репозитория контейнеров используется внутренний.

# Переменные

Могут быть переданы следующие параметры:

```docker_user``` - имя пользователя в репозитории, если требуется авторизация (не имеет значения по-умолчанию)

```docker_password``` - пароль пользователя в репозитории, если требуется авторизация (не имеет значения по-умолчанию)

Значение по-умолчанию для всех ниже перечисленных указано после двоеточия.

```docker_compose: "/usr/local/bin/docker-compose"``` - местоположение docker-compose

```dst_dir: "/cadvisor"``` - директория назначения, где будет хранится yml-файл

```cadvisor_image: "cadvisor:latest"``` - наименование образа

```docker_hub_port: 65222``` - порт подключения к внутреннему репозиторию

```docker_hub: "docker-test.xlab.jes.space:{{ docker_hub_port }}"``` - адрес репозитория

```cadvisor_ext_port: 9324``` - порт для системы мониторинга. Данный порт будет опрашивать хост с установленным Prometheus
